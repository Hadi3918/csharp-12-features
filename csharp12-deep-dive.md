
# 🌟 C# 12 Deep Dive — Write Cleaner Code with These New Features

C# 12, introduced with .NET 8, isn’t just a set of syntax tweaks — it brings real improvements that simplify your code, boost performance, and make the language more expressive.

In this article, we’ll explore five key features of C# 12, with clear explanations and **before-and-after examples** so you can start using them effectively in your projects.

---

## 🏗️ 1. Primary Constructors for Classes

> 🔄 Replaces verbose constructors with concise syntax  

### 📌 Old way:

```csharp
class Product
{
    private readonly string name;
    private readonly decimal price;

    public Product(string name, decimal price)
    {
        this.name = name;
        this.price = price;
    }

    public void PrintInfo() => Console.WriteLine($"{name}: ${price}");
}
```

### ✅ New way:

```csharp
class Product(string name, decimal price)
{
    public void PrintInfo() => Console.WriteLine($"{name}: ${price}");
}
```

---

## 🧩 2. Using Alias for Any Type

> 🔧 Create readable names for complex or generic types

```csharp
using IntList = List<int>;
using PersonTuple = (string Name, int Age);

IntList numbers = [1, 2, 3];
PersonTuple user = ("Alice", 30);

Console.WriteLine($"{user.Name} is {user.Age} years old.");
```

---

## ✨ 3. Extended Interpolated String Handlers

> 📦 More control, better performance for custom formatting

```csharp
[LogMessage($"User {userId} logged in at {DateTime.UtcNow}")]
void Authenticate(int userId) { /* ... */ }
```

---

## 🧺 4. Collection Expressions *(Preview)*

### 📌 Old way:

```csharp
var numbers = new List<int> { 1, 2, 3, 4 };
```

### ✅ New way:

```csharp
List<int> numbers = [1, 2, 3, 4];
int[] moreNumbers = [5, 6, 7];
```

---

## 🧷 5. `ref readonly` Parameters

```csharp
void PrintSpanLength(ref readonly Span<char> span)
{
    Console.WriteLine(span.Length);
}
```

---

## ✅ Summary Table

| Feature                     | What It Replaces / Enhances               | Benefits                         |
|----------------------------|--------------------------------------------|----------------------------------|
| Primary Constructors        | Traditional constructors in classes        | Less boilerplate, cleaner syntax |
| Using Alias for Any Type    | Old limited `using` alias                  | Better readability for generics  |
| Extended String Handlers    | String interpolation in more places        | Performance, flexibility         |
| Collection Expressions      | Verbose collection initializers            | Shorter syntax, JS-style init    |
| `ref readonly` Parameters   | `ref` + manual immutability enforcement    | Safe and fast struct handling    |

---

## 🔗 Resources & Next Steps

- 📦 Requires .NET 8 SDK  
- 💻 Try it on [.NET Fiddle](https://dotnetfiddle.net/) or in [Visual Studio 2022+](https://visualstudio.microsoft.com/)

---

### #CSharp12 #dotnet8 #cleanCode #modernCSharp #mediumDev
