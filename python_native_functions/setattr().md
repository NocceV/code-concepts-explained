# 📌 Understanding `setattr()` in Python

The `setattr()` function in Python is used to **set (assign) the value of an attribute** of an object dynamically.  
It’s very useful when you don’t know the attribute name beforehand or when it’s stored in a variable.

---

## 🔹 Syntax

```python
setattr(object, attribute_name, value)
```

- **object** → The object whose attribute you want to modify or create.  
- **attribute_name** → A string representing the attribute name.  
- **value** → The new value for the attribute.  

---

## 🔹 Basic Example

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

p = Person("Alice", 25)

# Direct assignment
p.age = 26

# Using setattr
setattr(p, "age", 30)

print(p.age)  # Output: 30
```

✅ Both approaches update the attribute.  

---

## 🔹 Adding New Attributes

If the attribute does not exist, `setattr()` will create it dynamically.

```python
setattr(p, "height", 1.75)
print(p.height)  # Output: 1.75
```

---

## 🔹 Dynamic Attribute Assignment

You can store attribute names in variables and set them dynamically:

```python
attr_name = "name"
setattr(p, attr_name, "Bob")

print(p.name)  # Output: Bob
```

This is useful when dealing with configs, user inputs, or dynamic objects.

---

## 🔹 Example with Methods

You can even assign **functions as attributes** to an object dynamically:

```python
class Calculator:
    pass

calc = Calculator()

def add(x, y):
    return x + y

# Dynamically add method
setattr(calc, "add", add)

print(calc.add(5, 7))  # Output: 12
```

---

## 🚀 Summary

- `setattr(obj, "attr", value)` → Sets (or creates) an attribute.  
- Can **update existing attributes** or **create new ones**.  
- Useful for **dynamic assignment** of values and methods.  
