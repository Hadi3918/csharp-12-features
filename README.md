<article>
  <h1>🌟 {article_title}</h1>
  <p><strong>C# 12</strong>, introduced with <strong>.NET 8</strong>, isn’t just a set of syntax tweaks — it brings real improvements that simplify your code, boost performance, and make the language more expressive.</p>

  <p>In this article, we’ll explore five key features of C# 12, with clear explanations and <strong>before-and-after examples</strong> so you can start using them effectively in your projects.</p>
  <hr/>

  <h2>🏗️ 1. Primary Constructors for Classes</h2>
  <blockquote>🔄 Replaces verbose constructors with concise syntax</blockquote>
  <h4>📌 Old way:</h4>
  <pre><code>class Product {{
    private readonly string name;
    private readonly decimal price;

    public Product(string name, decimal price) {{
        this.name = name;
        this.price = price;
    }}

    public void PrintInfo() => Console.WriteLine($"{'{'}name{'}'}: ${'{'}price{'}'}");
}}
</code></pre>
  <h4>✅ New way:</h4>
  <pre><code>class Product(string name, decimal price)
{{
    public void PrintInfo() => Console.WriteLine($"{'{'}name{'}'}: ${'{'}price{'}'}");
}}
</code></pre>

  <hr/>
  <h2>🧩 2. Using Alias for Any Type</h2>
  <blockquote>🔧 Create readable names for complex or generic types</blockquote>
  <pre><code>using IntList = List&lt;int&gt;;
using PersonTuple = (string Name, int Age);

IntList numbers = [1, 2, 3];
PersonTuple user = ("Alice", 30);

Console.WriteLine($"{'{'}user.Name{'}'} is {'{'}user.Age{'}'} years old.");
</code></pre>

  <hr/>
  <h2>✨ 3. Extended Interpolated String Handlers</h2>
  <blockquote>📦 More control, better performance for custom formatting</blockquote>
  <pre><code>[LogMessage($"User {'{'}userId{'}'} logged in at {'{'}DateTime.UtcNow{'}'}")]
void Authenticate(int userId) {{ /* ... */ }}
</code></pre>

  <hr/>
  <h2>🧺 4. Collection Expressions <em>(Preview)</em></h2>
  <h4>📌 Old way:</h4>
  <pre><code>var numbers = new List&lt;int&gt; {{ 1, 2, 3, 4 }};
</code></pre>
  <h4>✅ New way:</h4>
  <pre><code>List&lt;int&gt; numbers = [1, 2, 3, 4];
int[] moreNumbers = [5, 6, 7];
</code></pre>

  <hr/>
  <h2>🧷 5. <code>ref readonly</code> Parameters</h2>
  <pre><code>void PrintSpanLength(ref readonly Span&lt;char&gt; span)
{{
    Console.WriteLine(span.Length);
}}
</code></pre>

  <hr/>
  <h2>✅ Summary Table</h2>
  <table border="1" cellpadding="6">
    <tr>
      <th>Feature</th>
      <th>What It Replaces / Enhances</th>
      <th>Benefits</th>
    </tr>
    <tr>
      <td>Primary Constructors</td>
      <td>Traditional constructors in classes</td>
      <td>Less boilerplate, cleaner syntax</td>
    </tr>
    <tr>
      <td>Using Alias for Any Type</td>
      <td>Old limited <code>using</code> alias</td>
      <td>Better readability for generics</td>
    </tr>
    <tr>
      <td>Extended String Handlers</td>
      <td>String interpolation in more places</td>
      <td>Performance, flexibility</td>
    </tr>
    <tr>
      <td>Collection Expressions</td>
      <td>Verbose collection initializers</td>
      <td>Shorter syntax, JS-style init</td>
    </tr>
    <tr>
      <td><code>ref readonly</code> Parameters</td>
      <td><code>ref</code> + manual immutability enforcement</td>
      <td>Safe and fast struct handling</td>
    </tr>
  </table>

  <hr/>
  <h3>🔗 Resources & Next Steps</h3>
  <ul>
    <li>📦 Requires .NET 8 SDK</li>
    <li>💻 Try it on <a href="https://dotnetfiddle.net/">.NET Fiddle</a> or in <a href="https://visualstudio.microsoft.com/">Visual Studio 2022+</a></li>
  </ul>

  <p>#CSharp12 #dotnet8 #cleanCode #modernCSharp #mediumDev</p>
</article>
"""

html_path = "[/mnt/data/csharp12-medium-article.html](https://medium.com/@hadi.sharifzadeh1378/whats-new-in-c-12-deep-dive-into-the-most-useful-features-71ef9cabd4b8)"
with open(html_path, "w", encoding="utf-8") as f:
    f.write(html_content)
