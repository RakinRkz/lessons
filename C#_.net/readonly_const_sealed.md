# readonly vs const vs sealed


In C#, `readonly`, `const`, and `sealed` are different keywords with distinct purposes and usage scenarios. Let’s break down each one:

---

### **`const`**

* **Purpose** : Defines a compile-time constant.
* **Key Characteristics** :
* **Value is set at compile-time** and cannot be changed afterward.
* Implicitly `static`—you do not need to use the `static` keyword.
* Can only be a value type or a `string` (no reference types except `string`).
* Value must be assigned when declared.
* Can be accessed without an instance of the class.
* **Use Case** : For values that are truly constant and never change (e.g., mathematical constants, configuration keys).

#### Example:

```csharp
public class Example
{
    public const double Pi = 3.14159;
}
```

#### Key Limitation:

Changing a `const` requires recompiling all assemblies that reference it because the value is inlined at compile-time.

---

### **`readonly`**

**Purpose** : Allows the value of a field to be assigned either at declaration or in the constructor.

**Key Characteristics** :

* Value can only be set  **once** , either at the time of declaration or within a constructor.
* **Not implicitly `static`** , but can be combined with the `static` keyword for a static readonly field.
* Can be used with value types or reference types.
* The value is not inlined, meaning it can be changed without recompiling dependent assemblies.

#### Example:

```csharp
public class Example
{
    public readonly double Pi;

    public Example()
    {
        Pi = 3.14159; // Assigned in the constructor
    }
}
```

#### Use Case:

Use `readonly` for fields whose values might depend on runtime data but should not be modified afterward.

---

### **`sealed`**

* **Purpose** : Prevents a class from being inherited or prevents a method from being overridden.
* **Key Characteristics** :
* Applied to classes, methods, or properties.
* A `sealed` class  **cannot be a base class** .
* A `sealed` method in a derived class cannot be overridden further.
* Typically used to enforce immutability or to finalize an implementation.

#### Example: `sealed` class

```csharp
public sealed class FinalClass
{
    public void Display()
    {
        Console.WriteLine("This is a sealed class.");
    }
}
```

#### Example: `sealed` method

```csharp
public class BaseClass
{
    public virtual void Display() { }
}

public class DerivedClass : BaseClass
{
    public sealed override void Display() { }
}
```

#### Use Case:

Use `sealed` to:

* Optimize performance for classes not intended to be extended.
* Finalize the behavior of a method or property.

---

### **Comparison Table**

| Feature              | `const`             | `readonly`              | `sealed`                 |
| -------------------- | --------------------- | ------------------------- | -------------------------- |
| **Type**       | Compile-time constant | Runtime constant          | Inheritance control        |
| **Modifiable** | No                    | Yes (in constructor only) | Not applicable             |
| **Scope**      | Static by default     | Instance or static        | Class, method, or property |
| **Usage**      | For constant values   | For runtime immutability  | Prevent inheritance        |
| **Examples**   | `Pi = 3.14`         | `Pi = runtimeValue`     | `sealed class A {}`      |

---

### Key Recommendations:

1. Use `const` for values that never change and are known at compile-time.
2. Use `readonly` for values that are immutable after initialization but may vary between instances or be determined at runtime.
3. Use `sealed` to enforce finality on a class or method.
