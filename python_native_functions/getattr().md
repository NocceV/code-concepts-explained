# 📌 Understanding `getattr()` in Python

The `getattr()` function in Python is used to **get the value of an attribute** from an object dynamically.  
It’s very useful when you don’t know the attribute name beforehand or when it’s stored in a variable.

---

## 🔹 Syntax

```python
getattr(object, attribute_name, default)
```

- **object** → The object you want to inspect.  
- **attribute_name** → A string representing the attribute name.  
- **default (optional)** → Value to return if the attribute does not exist (avoids `AttributeError`).  

---

## 🔹 Basic Example

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

p = Person("Alice", 25)

# Direct access
print(p.name)       # Output: Alice

# Using getattr
print(getattr(p, "name"))  # Output: Alice
print(getattr(p, "age"))   # Output: 25
```

✅ Both approaches return the same result.  

---

## 🔹 Using Default Value

If the attribute does not exist, Python raises an `AttributeError`.  
To prevent this, you can pass a **default value**.

```python
print(getattr(p, "height", "Not available"))
# Output: Not available
```

Without the default, this would raise:
```python
# AttributeError: 'Person' object has no attribute 'height'
```

---

## 🔹 Dynamic Attribute Access

You can store attribute names in variables and access them dynamically:

```python
attr_name = "age"
print(getattr(p, attr_name))  # Output: 25
```

This is particularly useful when working with user inputs, configs, or reflection.

---

## 🔹 Example with Methods

`getattr()` can also be used to retrieve methods and call them dynamically:

```python
class Calculator:
    def add(self, x, y):
        return x + y

    def multiply(self, x, y):
        return x * y

calc = Calculator()

operation = "multiply"
method = getattr(calc, operation)

print(method(3, 4))  # Output: 12
```

Here, we dynamically selected the `multiply` method and executed it.

---

## 🚀 Summary

- `getattr(obj, "attr")` → Fetches the value of an attribute.  
- `getattr(obj, "attr", default)` → Returns `default` if the attribute doesn’t exist.  
- Useful for **dynamic access** to attributes and methods.  


