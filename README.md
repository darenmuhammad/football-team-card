# ***Football Team Card***

## Object.freeze()

`Object.freeze()` digunakan untuk membekukan suatu objek sehingga nilainya tidak bisa diubah, ditambahkan, atau dihapus setelah pembekuan dilakukan.

### Contoh Penggunaan:
```javascript
const person = { name: "John", age: 30 };
Object.freeze(person);
person.age = 40; // Tidak akan berubah
console.log(person.age); // Output: 30
```
> **Catatan:** `Object.freeze()` hanya membekukan properti di tingkat pertama. Properti yang berupa objek masih bisa diubah.

---

## Object Destructuring

Object Destructuring adalah fitur JavaScript yang memungkinkan kita mengekstrak properti dari sebuah objek ke dalam variabel dengan sintaks yang lebih ringkas.

### Contoh Penggunaan:
```javascript
const user = { name: "Alice", age: 25, city: "New York" };
const { name, age } = user;
console.log(name); // Output: Alice
console.log(age);  // Output: 25
```
> **Catatan:** Kita juga bisa memberikan default value saat destructuring:
```javascript
const { country = "USA" } = user;
console.log(country); // Output: USA
```

---

## Nested Object

Nested Object adalah objek yang memiliki objek lain sebagai propertinya.

### Contoh Penggunaan:
```javascript
const employee = {
  name: "David",
  position: "Developer",
  address: {
    city: "San Francisco",
    zip: "94105"
  }
};
console.log(employee.address.city); // Output: San Francisco
```

### Destructuring Nested Object:
```javascript
const { address: { city, zip } } = employee;
console.log(city); // Output: San Francisco
console.log(zip);  // Output: 94105
```
> **Catatan:** Jika properti dalam objek tidak ada, kita bisa memberikan default value:
```javascript
const { address: { country = "USA" } } = employee;
console.log(country); // Output: USA
```
