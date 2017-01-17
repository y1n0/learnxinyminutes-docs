---
language: markdown
contributors:
    - ["Dan Turkel", "http://danturkel.com/"]
    - ["Jacob Ward", "http://github.com/JacobCWard/"]
translators:
    - ["Ader", "https://github.com/y1n0"]
filename: markdown.md
lang: ar-ar
---


Markdown أنشأها "جون كروبر" في 2004. الهدف منها هو أن توفر أداة سهلة في 
القراءة والكتابة، وتُحول لـ ل.ت.ن.م (لغة ترميز النصوص المتشعبة - HTML) (ضمن صيغ أُخرى) بسهولة
(سيتم الإشارة في هذا الدليل لHTML بـ ل.ت.ن.م)

تختلف تأويلات مارك داونحسب كل محلل (parser). في هذا الدليل سنحاول أن نوضح ما إذا 
خاصية ما شاملة أو خاصة بحلل محدد 

- [عناصر ل.ت.ن.م](#html-elements)
- [العناوين](#headings)
- [تنميق النص البسيط](#simple-text-styles)
- [الفقرات](#paragraphs)
- [القوائم](#lists)
- [مجال الأكواد](#code-blocks)
- [القواعدة الأفقية](#horizontal-rule)
- [الروابط](#links)
- [الصور](#images)
- [منوعات](#miscellany)

## عناصر ل.ت.ن.م
مارك داون جزء من ل.ت.ن.م، ولذا فقكل ملف ل.ت.ن.م هو صيغة صحيحة من مارك داون

```markdown
<!--هذا يعني أنه يمكننا أن ندخل بعضا من عناصر ل.ت.ن.م في مارك داون،كعنصر 
التعليق، ولن يؤثر المحلل عليه عند التأويل. ومع ذلك، إذا أدخلت عنصرا من 
ل.ت.ن.م داخل مارك داون، لا يمكنك حينها استعمال تركيب مارك داون داخل محتويات 
هذا العنصر.-->
```

## العناوين

يمكنك وضع `<h1>` حتى `<h6>` عناصر ل.ت.ن.م بسهول عبر ابتداء السطر برمز الترقيم (#)

```markdown
# هذا عنوان <h1>
## هذا عنوان <h2>
### هذا عنوان <h3>
#### هذا عنوان <h4>
##### هذا عنوان <h5>
###### هذا عنوان <h6>
```
مارك داون مزود بطرق بديلة لتحديد العناوين

```markdown
هذا عنوان h1
=============

هذا عنوان h2
-------------
```

## تنميق النص البسيط

باستعمال مارك داون، يمكن تنميق النص ببساطة وجعله مائلا أو واضحا. 

```markdown
*هذا النص مائل.*
_وكذلك هذا النص._

**هذا النص واضح.**
__وكذلك هذا النص.__

***هذا النص يجمع بينهما معا.***
**_كهذا!_**
*__وهذا!__*
```

في محلل GitHub Flavored Markdown، الذي يستعمل لتأويل مارك داون على GitHub
هناك إمكانية تشطيب فوق النص:

```markdown
~~هذا النص مؤلٌ ومشطوب فوقه.~~
```
## الفقرات

الفقرات تكون عبارة عن سطر أو مجموعة من السطور، وتحدد الفقرات بتخطي سطر 
أو مجموعة من السطور البيضاء (خالية)

```markdown
هذه فقرة. رائع أن تكتب فقرات مطولة!

الأن نحن في الفقرة الثانية.
ما زلنا في الثانية!


والآن في الثالثة!
```

إذا أردت أن تضيف عصنر <br />، يمكنك أن تنهي الفقرة الحالية بمجموعة 
من الفراغات (اثنان أو أكثر) وعندها تبدأ الفقرة الموالية. 

```markdown
أُنهي هذه الفقرة بفراغات متتالية (ظلل النص لتظهر).   

وهنا <br /> فوقي!
```

يسهل إضافة مجال للاقتباس باستعمال الرمز > 

```markdown
> هذا مجال اقتباس. يمكنك اختيار إما أن
> تجعل السطور قصيرة يدويا وتبتدأ كل واحد منها ب `>` أو تتركها طويلة جدا ليُحدَّد عددها تلقائيا.
> It doesn't make a difference so long as they start with a `>`.
> فهذا لا يؤثر على مظهرها ما دامن مبتدأة بـ `>`.

> يمكنك أيضا استعمال اقتاباسات متداخلة
>> بجعلها متدرجة كهذا.
> أليس جد أنيق?

```

## القوائم
Unordered lists can be made using asterisks, pluses, or hyphens.
القوائم غير المرتبة تركب إما برمز النجمة، أو الزائد، أو الناقص

```markdown
* نقطة ما
* نقطة ما
* نقطة أخرى

أو

+ نقطة ما
+ نقطة ما
+ ونقطة أخرى

أو

- نقطة ما
- نقطة ما
- وآخر نقطة
```

القوائم المرقمة تركب بابتداء السطر برقم متبوع بنقطة.

```markdown
1. النقطة الأولى
2. النقطة الثانية
3. النقطة الثالثة
```

حتى وإن كانت الأرقام غير مرتبة أو متتابعة، أو حتى وإن كانت مكررة؛ 
مارك داون يقوم بالترقيم بانتظام حسب رقم السطر، ربما هذه فكرة غير جيدة.

```markdown
1. النقطة الأولى
1. النقطة الثانية
1. النقطة الثالثة
```
(هذا يأول تماما كالمثال السابق)

يمكنك كذلك استعمل قوائم فرعية

```markdown
1. النقطة الأولي
2. النقطة الثانية
3. النقطة الثالثة
    * نقطة فرعية
    * نقطة فرعية آخرى
4. النقطة الرابعة
```

هناك حتى قوائم المهام. وهي تنشئ خانات ل.ت.ن.م.

```markdown
الخانات التي لا تحتوي على x داخلها هي غير معلمة/محددة/مُنهاة
- [ ] المهمة الأولى لتنفذ.
- [ ] المهمة الثانية التي مازالت تحتاج أن تُنهى
الخانة في الأسفل ستنشئ خانة ل.ت.ن.م محددة.
- [x] وهذه المهمة تمت
```

## مجال الأكواد

يمكنك أن تحدد مجالا للأكواد (الذي يكون بعنصر ل.ت.ن.م: `<code>`) عبر
إضافة أربع فراغات أو التدرج في بداية السطر.

```markdown
    هذا عبارة عن كود
    وحتى هذا!
    (بالعربية؟)
```

يمكن كذلك إدراج تدرجات أخرى داخل الكود

```markdown
    my_array.each do |item|
        puts item
    end
```

الأكواد المندرجة في السطر يمكن أن تكتب باستعمال هذا الرمز: `

```markdown
أنت لا تدري حتى ما هو دور الدالة `go_to()` !
```

In GitHub Flavored Markdown, you can use a special syntax for code

<pre>
<code class="highlight">&#x60;&#x60;&#x60;ruby
def foobar
    puts "Hello world!"
end
&#x60;&#x60;&#x60;</code></pre>

The above text doesn't require indenting, plus GitHub will use syntax
highlighting of the language you specify after the \`\`\`

## Horizontal rule

Horizontal rules (`<hr/>`) are easily added with three or more asterisks or 
hyphens, with or without spaces.

```markdown
***
---
- - -
****************
```

## Links

One of the best things about markdown is how easy it is to make links. Put
the text to display in hard brackets [] followed by the url in parentheses ()

```markdown
[Click me!](http://test.com/)
```
You can also add a link title using quotes inside the parentheses.

```markdown
[Click me!](http://test.com/ "Link to Test.com")
```
Relative paths work too.

```markdown
[Go to music](/music/).
```

Markdown also supports reference style links.

<pre><code class="highlight">&#x5b;<span class="nv">Click this link</span>][<span class="ss">link1</span>] for more info about it!
&#x5b;<span class="nv">Also check out this link</span>][<span class="ss">foobar</span>] if you want to.

&#x5b;<span class="nv">link1</span>]: <span class="sx">http://test.com/</span> <span class="nn">"Cool!"</span>
&#x5b;<span class="nv">foobar</span>]: <span class="sx">http://foobar.biz/</span> <span class="nn">"Alright!"</span></code></pre>

The title can also be in single quotes or in parentheses, or omitted
entirely. The references can be anywhere in your document and the reference IDs
can be anything so long as they are unique.

There is also "implicit naming" which lets you use the link text as the id.

<pre><code class="highlight">&#x5b;<span class="nv">This</span>][] is a link.

&#x5b;<span class="nv">this</span>]: <span class="sx">http://thisisalink.com/</span></code></pre>

But it's not that commonly used.

## Images
Images are done the same way as links but with an exclamation point in front!

```markdown
![This is the alt-attribute for my image](http://imgur.com/myimage.jpg "An optional title")
```

And reference style works as expected.

<pre><code class="highlight">!&#x5b;<span class="nv">This is the alt-attribute.</span>][<span class="ss">myimage</span>]

&#x5b;<span class="nv">myimage</span>]: <span class="sx">relative/urls/cool/image.jpg</span> <span class="nn">"if you need a title, it's here"</span></code></pre>
## Miscellany
### Auto-links

```markdown
<http://testwebsite.com/> is equivalent to
[http://testwebsite.com/](http://testwebsite.com/)
```

### Auto-links for emails

```markdown
<foo@bar.com>
```

### Escaping characters

```markdown
I want to type *this text surrounded by asterisks* but I don't want it to be
in italics, so I do this: \*this text surrounded by asterisks\*.
```

### Keyboard keys

In GitHub Flavored Markdown, you can use a `<kbd>` tag to represent keyboard 
keys.

```markdown
Your computer crashed? Try sending a
<kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Del</kbd>
```
### Tables

Tables are only available in GitHub Flavored Markdown and are slightly
cumbersome, but if you really want it:

```markdown
| Col1         | Col2     | Col3          |
| :----------- | :------: | ------------: |
| Left-aligned | Centered | Right-aligned |
| blah         | blah     | blah          |
```
or, for the same results

```markdown
Col 1 | Col2 | Col3
:-- | :-: | --:
Ugh this is so ugly | make it | stop
```

---
For more info, check out John Gruber's official post of syntax [here](http://daringfireball.net/projects/markdown/syntax) and Adam Pritchard's great cheatsheet [here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).
