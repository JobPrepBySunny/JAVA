
## 📚 Java Methods and Functions Cheat Sheet

This document provides a one-line explanation and a short example for common Java methods.

---

## 1. Core Java (`java.lang`)

### Object Class (base of all classes)

* **`toString()`** $\rightarrow$ Returns a string representation of the object.
    * *Example:* `System.out.println(myObject);`
* **`equals(obj)`** $\rightarrow$ Checks if this object is the same as the argument object.
    * *Example:* `myObject1.equals(myObject2);`
* **`hashCode()`** $\rightarrow$ Returns a hash code value for the object.
    * *Example:* `myObject.hashCode();`
* **`clone()`** $\rightarrow$ Creates and returns a copy of this object.
    * *Example:* `MyClass newObj = (MyClass) myObject.clone();`
* **`getClass()`** $\rightarrow$ Returns the runtime class of this object.
    * *Example:* `myObject.getClass().getName();`
* **`wait()`, `notify()`, `notifyAll()`** $\rightarrow$ Methods for inter-thread communication.
    * *Example:* `myObject.wait();`

### String Class

* **`length()`** $\rightarrow$ Returns the number of characters in the string.
    * *Example:* `"hello".length(); // 5`
* **`charAt(i)`** $\rightarrow$ Returns the character at the specified index.
    * *Example:* `"hello".charAt(1); // 'e'`
* **`substring(start, end)`** $\rightarrow$ Returns a new string that is a substring of this string.
    * *Example:* `"hello".substring(1, 3); // "el"`
* **`contains(str)`** $\rightarrow$ Returns true if the string contains the specified sequence of characters.
    * *Example:* `"hello".contains("ell"); // true`
* **`equals(s2)`** $\rightarrow$ Compares two strings for content equality, case-sensitive.
    * *Example:* `"hello".equals("HELLO"); // false`
* **`equalsIgnoreCase(s2)`** $\rightarrow$ Compares two strings, ignoring case considerations.
    * *Example:* `"hello".equalsIgnoreCase("HELLO"); // true`
* **`toUpperCase()`, `toLowerCase()`** $\rightarrow$ Converts the string to uppercase or lowercase.
    * *Example:* `"Hello".toUpperCase(); // "HELLO"`
* **`trim()`** $\rightarrow$ Returns a copy of the string with leading and trailing whitespace removed.
    * *Example:* `" hello ".trim(); // "hello"`
* **`split(regex)`** $\rightarrow$ Splits a string into an array of substrings based on a delimiter.
    * *Example:* `"a,b,c".split(","); // "a", "b", "c"`
* **`replace(old, new)`** $\rightarrow$ Returns a new string resulting from replacing all occurrences of a character/sequence.
    * *Example:* `"java".replace('a', 'o'); // "jovo"`
* **`indexOf(ch) / lastIndexOf(ch)`** $\rightarrow$ Returns the index of the first or last occurrence of the specified character.
    * *Example:* `"hello".indexOf('l'); // 2`

---

## 2. Collections Framework (`java.util`)

### List / ArrayList

* **`add(e)`, `addAll(c)`** $\rightarrow$ Adds an element or all elements from a collection to the list.
    * *Example:* `list.add("apple");`
* **`get(i)`, `set(i,e)`** $\rightarrow$ Returns the element at the specified position or replaces it with a new element.
    * *Example:* `list.get(0);`
* **`remove(i)`, `removeAll(c)`** $\rightarrow$ Removes an element at a specific index or all elements from a collection.
    * *Example:* `list.remove(0);`
* **`size()`, `isEmpty()`** $\rightarrow$ Returns the number of elements or checks if the list is empty.
    * *Example:* `list.size();`
* **`contains(e)`, `indexOf(e)`** $\rightarrow$ Checks if the list contains an element or returns its index.
    * *Example:* `list.contains("apple");`

### Set / HashSet

* **`add(e)`, `remove(e)`** $\rightarrow$ Adds an element to the set or removes it.
    * *Example:* `set.add("A");`
* **`contains(e)`, `size()`** $\rightarrow$ Checks if the set contains an element or returns the number of elements.
    * *Example:* `set.contains("A");`
* **`clear()`, `isEmpty()`** $\rightarrow$ Removes all elements from the set or checks if it's empty.
    * *Example:* `set.clear();`

### Map / HashMap

* **`put(k,v)`, `putAll(m)`** $\rightarrow$ Associates a key with a value or copies all mappings from another map.
    * *Example:* `map.put("A", 1);`
* **`get(k)`, `getOrDefault(k,v)`** $\rightarrow$ Returns the value to which the specified key is mapped or a default value.
    * *Example:* `map.get("A"); // 1`
* **`remove(k)`** $\rightarrow$ Removes the mapping for a key from the map.
    * *Example:* `map.remove("A");`
* **`containsKey(k)`, `containsValue(v)`** $\rightarrow$ Returns true if the map contains the key or value.
    * *Example:* `map.containsKey("A");`
* **`size()`, `isEmpty()`** $\rightarrow$ Returns the number of key-value mappings or checks if the map is empty.
    * *Example:* `map.size();`
* **`keySet()`, `values()`, `entrySet()`** $\rightarrow$ Returns a set of the keys, a collection of the values, or a set of the key-value pairs.
    * *Example:* `map.keySet();`

### Collections Utility

* **`sort(list)`** $\rightarrow$ Sorts the elements in a list in ascending order.
    * *Example:* `Collections.sort(myList);`
* **`reverse(list)`** $\rightarrow$ Reverses the order of the elements in a list.
    * *Example:* `Collections.reverse(myList);`
* **`shuffle(list)`** $\rightarrow$ Randomly shuffles the elements in a list.
    * *Example:* `Collections.shuffle(myList);`
* **`max(list)`, `min(list)`** $\rightarrow$ Returns the maximum or minimum element in a list.
    * *Example:* `Collections.max(myList);`
* **`frequency(list,e)`** $\rightarrow$ Returns the number of times an element occurs in a list.
    * *Example:* `Collections.frequency(myList, "A");`
* **`swap(list,i,j)`** $\rightarrow$ Swaps the elements at the specified positions in a list.
    * *Example:* `Collections.swap(myList, 0, 1);`

### Arrays Utility

* **`sort(arr)`** $\rightarrow$ Sorts the elements in an array in ascending order.
    * *Example:* `Arrays.sort(myArray);`
* **`binarySearch(arr, key)`** $\rightarrow$ Searches a sorted array for the specified value.
    * *Example:* `Arrays.binarySearch(myArray, 5);`
* **`copyOf(arr, newLen)`** $\rightarrow$ Copies the specified array, truncating or padding with zeros.
    * *Example:* `Arrays.copyOf(myArray, 10);`
* **`copyOfRange(arr, s, e)`** $\rightarrow$ Copies the specified range of the array into a new array.
    * *Example:* `Arrays.copyOfRange(myArray, 2, 5);`
* **`equals(arr1, arr2)`** $\rightarrow$ Checks if two arrays are equal based on their contents.
    * *Example:* `Arrays.equals(arr1, arr2);`
* **`fill(arr, val)`** $\rightarrow$ Assigns the specified value to each element of the array.
    * *Example:* `Arrays.fill(myArray, 0);`
* **`toString(arr)`** $\rightarrow$ Returns a string representation of the contents of the array.
    * *Example:* `System.out.println(Arrays.toString(myArray));`

---

## 3. Input / Output

### Scanner Class

* **`next()`, `nextLine()`** $\rightarrow$ Reads the next token or the rest of the line from the input.
    * *Example:* `String token = scanner.next();`
* **`nextInt()`, `nextDouble()`, `nextBoolean()`** $\rightarrow$ Scans the next token as an `int`, `double`, or `boolean`.
    * *Example:* `int num = scanner.nextInt();`
* **`hasNext()`** $\rightarrow$ Returns true if the scanner has another token in its input.
    * *Example:* `while (scanner.hasNext()) { ... }`

### System Class

* **`System.out.println(x)`** $\rightarrow$ Prints a line of text to the standard output.
    * *Example:* `System.out.println("Hello");`
* **`System.err.println(x)`** $\rightarrow$ Prints a line of text to the standard error stream.
    * *Example:* `System.err.println("Error!");`
* **`System.currentTimeMillis()`** $\rightarrow$ Returns the current time in milliseconds since the Unix epoch.
    * *Example:* `long time = System.currentTimeMillis();`
* **`System.gc()`** $\rightarrow$ Runs the garbage collector.
    * *Example:* `System.gc();`

### File Class

* **`createNewFile()`, `delete()`** $\rightarrow$ Atomically creates a new, empty file or deletes the file.
    * *Example:* `file.createNewFile();`
* **`exists()`, `getName()`, `getPath()`** $\rightarrow$ Checks if the file exists, returns its name, or returns its path.
    * *Example:* `file.exists();`
* **`length()`** $\rightarrow$ Returns the length of the file in bytes.
    * *Example:* `file.length();`
* **`list()`, `mkdir()`, `mkdirs()`** $\rightarrow$ Returns an array of files in the directory, or creates a directory or directories.
    * *Example:* `file.mkdir();`

### FileReader / FileWriter

* **`read()`, `readLine()`** $\rightarrow$ Reads a single character or a line of text.
    * *Example:* `int charCode = reader.read();`
* **`write(str)`** $\rightarrow$ Writes a string to the output stream.
    * *Example:* `writer.write("Hello");`
* **`flush()`, `close()`** $\rightarrow$ Flushes the stream's buffer or closes the stream.
    * *Example:* `writer.close();`

---

## 4. Threads & Concurrency

### Thread Class

* **`start()`, `run()`** $\rightarrow$ Starts the thread's execution; `run()` contains the code to be executed.
    * *Example:* `thread.start();`
* **`sleep(ms)`** $\rightarrow$ Pauses the current thread for a specified number of milliseconds.
    * *Example:* `Thread.sleep(1000);`
* **`join()`** $\rightarrow$ Waits for the thread to die (finish its execution).
    * *Example:* `thread.join();`
* **`interrupt()`** $\rightarrow$ Interrupts the thread.
    * *Example:* `thread.interrupt();`
* **`isAlive()`** $\rightarrow$ Tests if the thread is alive (has been started and has not yet died).
    * *Example:* `thread.isAlive();`
* **`getName()`, `setName()`** $\rightarrow$ Returns or sets the thread's name.
    * *Example:* `thread.setName("MyThread");`
* **`getPriority()`, `setPriority()`** $\rightarrow$ Returns or sets the thread's priority.
    * *Example:* `thread.setPriority(1);`

---

## 5. Other Useful APIs

### Date & Time (`java.time`)

* **`LocalDate.now()`, `LocalTime.now()`, `LocalDateTime.now()`** $\rightarrow$ Gets the current date, time, or date and time.
    * *Example:* `LocalDate today = LocalDate.now();`
* **`plusDays(n)`, `minusDays(n)`** $\rightarrow$ Adds or subtracts a specified number of days.
    * *Example:* `today.plusDays(1);`
* **`getYear()`, `getMonth()`, `getDayOfWeek()`** $\rightarrow$ Returns the year, month, or day of the week.
    * *Example:* `today.getYear();`

### Files (`java.nio.file`)

* **`Files.readAllBytes(path)`** $\rightarrow$ Reads all the bytes from a file.
    * *Example:* `Files.readAllBytes(myPath);`
* **`Files.readAllLines(path)`** $\rightarrow$ Reads all lines from a file.
    * *Example:* `Files.readAllLines(myPath);`
* **`Files.write(path, data)`** $\rightarrow$ Writes bytes or lines to a file.
    * *Example:* `Files.write(myPath, myData);`
* **`Files.exists(path)`** $\rightarrow$ Tests if a file exists.
    * *Example:* `Files.exists(myPath);`
* **`Files.copy(src, dest)`** $\rightarrow$ Copies a file from the source path to the destination path.
    * *Example:* `Files.copy(srcPath, destPath);`
* **`Files.delete(path)`** $\rightarrow$ Deletes a file.
    * *Example:* `Files.delete(myPath);`

### SQL (`java.sql`)

* **`Connection.createStatement()`** $\rightarrow$ Creates a statement object for sending SQL statements to the database.
    * *Example:* `Statement stmt = connection.createStatement()`
* **`Statement.executeQuery(sql)`** $\rightarrow$ Executes an SQL query that returns a `ResultSet` object.
    * *Example:* `ResultSet rs = stmt.executeQuery("SELECT * FROM users");`
* **`Statement.executeUpdate(sql)`** $\rightarrow$ Executes an SQL statement for DDL or DML commands (e.g., INSERT, UPDATE, DELETE).
    * *Example:* `stmt.executeUpdate("INSERT INTO users VALUES ('John')");`
* **`ResultSet.next()`, `ResultSet.getString(col)`** $\rightarrow$ Moves the cursor to the next row; gets the value of the specified column as a string.
    * *Example:* `while (rs.next()) { String name = rs.getString("name"); }`

---
