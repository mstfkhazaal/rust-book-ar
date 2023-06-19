# Introduction

> Note: This edition of the book is the same as [The Rust Programming
> Language][nsprust] available in print and ebook format from [No Starch
> Press][nsp].

[nsprust]: https://nostarch.com/rust-programming-language-2nd-edition
[nsp]: https://nostarch.com/

Welcome to *The Rust Programming Language*, an introductory book about Rust.
The Rust programming language helps you write faster, more reliable software.
High-level ergonomics and low-level control are often at odds in programming
language design; Rust challenges that conflict. Through balancing powerful
technical capacity and a great developer experience, Rust gives you the option
to control low-level details (such as memory usage) without all the hassle
traditionally associated with such control.

## Who Rust Is For

Rust is ideal for many people for a variety of reasons. Let’s look at a few of
the most important groups.

### Teams of Developers

Rust is proving to be a productive tool for collaborating among large teams of
developers with varying levels of systems programming knowledge. Low-level code
is prone to various subtle bugs, which in most other languages can be caught
only through extensive testing and careful code review by experienced
developers. In Rust, the compiler plays a gatekeeper role by refusing to
compile code with these elusive bugs, including concurrency bugs. By working
alongside the compiler, the team can spend their time focusing on the program’s
logic rather than chasing down bugs.

Rust also brings contemporary developer tools to the systems programming world:

* Cargo, the included dependency manager and build tool, makes adding,
  compiling, and managing dependencies painless and consistent across the Rust
  ecosystem.
* The Rustfmt formatting tool ensures a consistent coding style across
  developers.
* The Rust Language Server powers Integrated Development Environment (IDE)
  integration for code completion and inline error messages.

By using these and other tools in the Rust ecosystem, developers can be
productive while writing systems-level code.

### Students

Rust is for students and those who are interested in learning about systems
concepts. Using Rust, many people have learned about topics like operating
systems development. The community is very welcoming and happy to answer
student questions. Through efforts such as this book, the Rust teams want to
make systems concepts more accessible to more people, especially those new to
programming.

### Companies

Hundreds of companies, large and small, use Rust in production for a variety of
tasks, including command line tools, web services, DevOps tooling, embedded
devices, audio and video analysis and transcoding, cryptocurrencies,
bioinformatics, search engines, Internet of Things applications, machine
learning, and even major parts of the Firefox web browser.

### Open Source Developers

Rust is for people who want to build the Rust programming language, community,
developer tools, and libraries. We’d love to have you contribute to the Rust
language.

### People Who Value Speed and Stability

Rust is for people who crave speed and stability in a language. By speed, we
mean both how quickly Rust code can run and the speed at which Rust lets you
write programs. The Rust compiler’s checks ensure stability through feature
additions and refactoring. This is in contrast to the brittle legacy code in
languages without these checks, which developers are often afraid to modify. By
striving for zero-cost abstractions, higher-level features that compile to
lower-level code as fast as code written manually, Rust endeavors to make safe
code be fast code as well.

The Rust language hopes to support many other users as well; those mentioned
here are merely some of the biggest stakeholders. Overall, Rust’s greatest
ambition is to eliminate the trade-offs that programmers have accepted for
decades by providing safety *and* productivity, speed *and* ergonomics. Give
Rust a try and see if its choices work for you.

## Who This Book Is For

This book assumes that you’ve written code in another programming language but
doesn’t make any assumptions about which one. We’ve tried to make the material
broadly accessible to those from a wide variety of programming backgrounds. We
don’t spend a lot of time talking about what programming *is* or how to think
about it. If you’re entirely new to programming, you would be better served by
reading a book that specifically provides an introduction to programming.

## How to Use This Book

In general, this book assumes that you’re reading it in sequence from front to
back. Later chapters build on concepts in earlier chapters, and earlier
chapters might not delve into details on a particular topic but will revisit
the topic in a later chapter.

You’ll find two kinds of chapters in this book: concept chapters and project
chapters. In concept chapters, you’ll learn about an aspect of Rust. In project
chapters, we’ll build small programs together, applying what you’ve learned so
far. Chapters 2, 12, and 20 are project chapters; the rest are concept chapters.

Chapter 1 explains how to install Rust, how to write a “Hello, world!” program,
and how to use Cargo, Rust’s package manager and build tool. Chapter 2 is a
hands-on introduction to writing a program in Rust, having you build up a
number guessing game. Here we cover concepts at a high level, and later
chapters will provide additional detail. If you want to get your hands dirty
right away, Chapter 2 is the place for that. Chapter 3 covers Rust features
that are similar to those of other programming languages, and in Chapter 4
you’ll learn about Rust’s ownership system. If you’re a particularly meticulous
learner who prefers to learn every detail before moving on to the next, you
might want to skip Chapter 2 and go straight to Chapter 3, returning to Chapter
2 when you’d like to work on a project applying the details you’ve learned.

Chapter 5 discusses structs and methods, and Chapter 6 covers enums, `match`
expressions, and the `if let` control flow construct. You’ll use structs and
enums to make custom types in Rust.

In Chapter 7, you’ll learn about Rust’s module system and about privacy rules
for organizing your code and its public Application Programming Interface
(API). Chapter 8 discusses some common collection data structures that the
standard library provides, such as vectors, strings, and hash maps. Chapter 9
explores Rust’s error-handling philosophy and techniques.

Chapter 10 digs into generics, traits, and lifetimes, which give you the power
to define code that applies to multiple types. Chapter 11 is all about testing,
which even with Rust’s safety guarantees is necessary to ensure your program’s
logic is correct. In Chapter 12, we’ll build our own implementation of a subset
of functionality from the `grep` command line tool that searches for text
within files. For this, we’ll use many of the concepts we discussed in the
previous chapters.

Chapter 13 explores closures and iterators: features of Rust that come from
functional programming languages. In Chapter 14, we’ll examine Cargo in more
depth and talk about best practices for sharing your libraries with others.
Chapter 15 discusses smart pointers that the standard library provides and the
traits that enable their functionality.

In Chapter 16, we’ll walk through different models of concurrent programming
and talk about how Rust helps you to program in multiple threads fearlessly.
Chapter 17 looks at how Rust idioms compare to object-oriented programming
principles you might be familiar with.

Chapter 18 is a reference on patterns and pattern matching, which are powerful
ways of expressing ideas throughout Rust programs. Chapter 19 contains a
smorgasbord of advanced topics of interest, including unsafe Rust, macros, and
more about lifetimes, traits, types, functions, and closures.

In Chapter 20, we’ll complete a project in which we’ll implement a low-level
multithreaded web server!

Finally, some appendices contain useful information about the language in a
more reference-like format. Appendix A covers Rust’s keywords, Appendix B
covers Rust’s operators and symbols, Appendix C covers derivable traits
provided by the standard library, Appendix D covers some useful development
tools, and Appendix E explains Rust editions. In Appendix F, you can find
translations of the book, and in Appendix G we’ll cover how Rust is made and
what nightly Rust is.

There is no wrong way to read this book: if you want to skip ahead, go for it!
You might have to jump back to earlier chapters if you experience any
confusion. But do whatever works for you.

<span id="ferris"></span>

An important part of the process of learning Rust is learning how to read the
error messages the compiler displays: these will guide you toward working code.
As such, we’ll provide many examples that don’t compile along with the error
message the compiler will show you in each situation. Know that if you enter
and run a random example, it may not compile! Make sure you read the
surrounding text to see whether the example you’re trying to run is meant to
error. Ferris will also help you distinguish code that isn’t meant to work:

| Ferris                                                                                                           | Meaning                                          |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <img src="img/ferris/does_not_compile.svg" class="ferris-explain" alt="Ferris with a question mark"/>            | This code does not compile!                      |
| <img src="img/ferris/panics.svg" class="ferris-explain" alt="Ferris throwing up their hands"/>                   | This code panics!                                |
| <img src="img/ferris/not_desired_behavior.svg" class="ferris-explain" alt="Ferris with one claw up, shrugging"/> | This code does not produce the desired behavior. |

In most situations, we’ll lead you to the correct version of any code that
doesn’t compile.

## Source Code

The source files from which this book is generated can be found on
[GitHub][book].

[book]: https://github.com/rust-lang/book/tree/main/src

# مقدمة

> ملاحظة: هذا الإصدار من الكتاب هو نفسه كتاب [لغة برمجة Rust][nsprust] المتاح في الطبعة المطبوعة والإلكترونية من [ناشر No Starch][nsp].

[nsprust]: https://nostarch.com/rust-programming-language-2nd-edition
[nsp]: https://nostarch.com/

مرحبًا بك في كتاب "لغة برمجة Rust"، وهو كتاب مقدمة عن Rust. لغة برمجة Rust تساعدك في كتابة برمجيات أسرع وأكثر موثوقية. عادةً ما تتعارض الإريجونومية على المستوى العالي والتحكم على المستوى المنخفض في تصميم لغات البرمجة. ولكن Rust يتحدى هذا الصراع. من خلال توازن القدرات التقنية القوية وتجربة المطور الرائعة، يمنحك Rust الخيار للتحكم في التفاصيل منخفضة المستوى (مثل استخدام الذاكرة) دون كل الصعوبات المرتبطة تقليديًا بهذا النوع من التحكم.

## لمن يصلح Rust؟

تعتبر Rust مثالية للعديد من الأشخاص لأسباب مختلفة. دعنا نلقي نظرة على بعض المجموعات الأكثر أهمية.

### فِرَق المطورين

ثبت أن Rust هي أداة منتجة للتعاون بين فِرَق كبيرة من المطورين ذوي مستويات مختلفة من معرفة برمجة الأنظمة. تتعرض الشيفرة منخفضة المستوى لمجموعة متنوعة من الأخطاء الدقيقة، والتي في معظم لغات البرمجة الأخرى يمكن اكتشافها فقط من خلال اختبار شامل ومراجعة شيفرة دقيقة من قبل المطورين ذوي الخبرة. في Rust، يقوم المترجم بدور حارس يرفض تجميع الشيفرة التي تحتوي على هذه الأخطاء الصعبة، بما في ذلك أخطاء التوازي. من خلال العمل جنبًا إلى جنب مع المترجم، يمكن للفريق أن يستغل وقته في التركيز على منطق البرنامج بدلاً من مطاردة الأخطاء.

Rust يقدم أيضًا أدوات المطور المعاصرة في عالم برمجة الأنظمة:

- Cargo ، أداة إدارة التبعيات وأداة البناء المضمنة ، تجعل إضافة وتجميع وإدارة التبعيات سهلة ومتسقة في نظام Rust البيئي.
- أداة التنسيق Rustfmt تضمن أسلوبًا برمجيًا متسقًا بين المطورين.
- خادم لغة Rust يمكّن دمج بيئة التطوير المتكاملة (IDE) لإكمال الشفرة وعرض رسائل الخطأ المضمنة.

من خلال استخدام هذه الأدوات وغيرها في بيئة Rust ، يمكن للمطورين أن يكونوا منتجين أثناء كتابة شيفرة المستوى النظام.

### الطلاب

Rust هي للطلاب وأولئك الذين يهتمون بتعلم مفاهيم الأنظمة. باستخدام Rust ، تعلم العديد من الأشخاص حول مواضيع مثل تطوير أنظمة التشغيل. المجتمع مرحب جدًا وسعيد بالإجابة على أسئلة الطلاب. من خلال جهود مثل هذا الكتاب ، يرغب فريق Rust في جعل مفاهيم الأنظمة أكثر إمكانية الوصول للمزيد من الناس ، خاصةً أولئك الذين جددوا في مجال البرمجة.

### الشركات

يستخدم المئات من الشركات الكبيرة والصغيرة Rust في الإنتاج لأغراض متنوعة ، بما في ذلك أدوات سطر الأوامر ، وخدمات الويب ، وأدوات DevOps ، والأجهزة المضمنة ، وتحليل الصوت والفيديو وتحويله ، والعملات المشفرة ، وعلم المعلومات الحيوية ، ومحركات البحث ، وتطبيقات الأشياء المتصلة بالإنترنت ، والتعلم الآلي ، وحتى أجزاء رئيسية من متصفح الويب Firefox.

### مطورو البرمجيات مفتوحة المصدر

Rust هي لأولئك الذين يرغبون في بناء لغة برمجة Rust ومجتمعها وأدوات المطور والمكتبات. نحب أن نرى مساهمتك في لغة Rust.

### الأشخاص الذين يقدرون السرعة والاستقرار

Rust هي لأولئك الذين يتوقون إلى السرعة والاستقرار في اللغة. من خلال السرعة ، نعني سرعة تشغيل الشيفرة Rust وسرعة كتابة البرامج باستخدامها. يضمن فحص المترجم في Rust الاستقرار من خلال إضافة الميزات وإعادة التنظيم. هذا في مقابل الشيفرة القديمة والهشة في اللغات التي لا توفر هذه الفحوصات ، والتي يخشى المطورون غالبًا تعديلها. من خلال السعي للحصول على التجاويف بتكلفة صفرية ، وهي ميزات عالية المستوى تترجم إلى شيفرة على مستوى أدنى بنفس سرعة الشيفرة المكتوبة يدويًا ، تسعى Rust لجعل الشيفرة الآمنة شيفرة سريعة أيضًا.

اللغة Rust تأمل أيضًا في دعم العديد من المستخدمين الآخرين ؛ الذين ذكرناهم هنا هم ببساطة بعض أكبر أصحاب المصلحة. بشكل عام ، يهدف Rust إلى القضاء على التنازلات التي قبلها المبرمجون لعقود عن طريق توفير السلامة والإنتاجية والسرعة والسهولة. قم بتجربة Rust وشاهد ما إذا كانت اختياراتها تناسبك.

## لمن يصلح هذا الكتاب

يفترض هذا الكتاب أنك كتبت شيفرة في لغة برمجة أخرى ولكنه لا يفترض أي افتراضات حول اللغة التي تستخدمها. حاولنا جعل المواد متاحة على نطاق واسع لأولئك الذين لديهم خلفيات برمجية متنوعة. لا نقضي الكثير من الوقت في التحدث عن ما هي البرمجة أو كيفية التفكير فيها. إذا كنت جديدًا تمامًا في البرمجة ، فسيكون من الأفضل أن تقرأ كتابًا يوفر بالتحديد مقدمة في البرمجة.

## كيفية استخدام هذا الكتاب

بشكل عام ، يفترض هذا الكتاب أنك تقرأه بالتسلسل من الأمام إلى الخلف. تبنى الفصول اللاحقة على المفاهيم الموجودة في الفصول السابقة ، وقد لا تتناول الفصول السابقة تفصيلًا في موضوع معين ولكنها ستعود إلى هذا الموضوع في فصل لاحق.

ستجد نوعين من الفصول في هذا الكتاب: فصول المفاهيم وفصول المشروع. في فصول المفاهيم ، ستتعلم عن جانب من جوانب لغة Rust. في فصول المشروع ، سنبني برامج صغيرة معًا ، ونطبق ما تعلمته حتى الآن. الفصول 2 و 12 و 20 هي فصول المشروع. بقية الفصول هي فصول المفاهيم.

يشرح الفصل 1 كيفية تثبيت Rust وكتابة برنامج "Hello, world!" وكيفية استخدام Cargo ، أداة الإدارة وبناء الحزم في Rust. الفصل 2 هو مقدمة عملية لكتابة برنامج في Rust ، حيث تقوم ببناء لعبة تخمين الأرقام. هنا نغطي المفاهيم على مستوى عالٍ ، وستوفر الفصول اللاحقة تفاصيل إضافية. إذا كنت ترغب في التعامل مع الشيفرة فورًا ، فإن الفصل 2 هو المكان المناسب لذلك. يتناول الفصل 3 الميزات في Rust التي تشبه تلك الموجودة في لغات أخرى ، بما في ذلك التعليمات الشرطية والحلقات.

الفصل 5 يتناول المنشآت (structs) والوظائف (methods)، والفصل 6 يغطي التعابير المطابقة (match expressions) وبنية التحكم (control flow) `if let`. ستستخدم المنشآت والتعدادات (enums) لإنشاء أنواع مخصصة في Rust.

في الفصل 7، ستتعرف على نظام الوحدات (module system) في Rust وعلى قواعد الخصوصية لتنظيم الكود وواجهة برمجة التطبيقات (API) العامة له. يتناول الفصل 8 بعض هياكل البيانات المشتركة التي توفرها المكتبة القياسية في Rust، مثل النوافذ (vectors) والسلاسل (strings) والخرائط الهاش (hash maps). يستكشف الفصل 9 فلسفة وتقنيات التعامل مع الأخطاء في Rust.

يتعمق الفصل 10 في المفاهيم العامة (generics) والصفات (traits) وفترات الحياة (lifetimes)، والتي تمنحك القدرة على تعريف الكود الذي ينطبق على أنواع متعددة. يتعلق الفصل 11 بالاختبار، والذي يعد ضرورياً حتى مع ضمانات السلامة في Rust لضمان صحة منطق برنامجك. في الفصل 12، سنقوم ببناء تنفيذنا الخاص لمجموعة من وظائف أداة سطر الأوامر "grep" التي تبحث عن نص داخل الملفات. سنستخدم في ذلك الكثير من المفاهيم التي نناقشها في الفصول السابقة.

يتناول الفصل 13 الإغلاقات (closures) والمكررات (iterators): الميزات في Rust التي تأتي من لغات البرمجة الوظيفية. في الفصل 14، سنناقش أداة Cargo بمزيد من التفصيل ونتحدث عن أفضل الممارسات لمشاركة المكتبات الخاصة بك مع الآخرين. يتناول الفصل 15 العناصر الذكية (smart pointers) التي توفرها المكتبة القياسية والصفات التي تمكن وظائفها.

في الفصل 16، سنستعرض نماذج مختلفة للبرمجة المتزامنة ونتحدث عن كيفية مساعدة Rust لك في برمجة خيوط متعددة دون خوف. ينظر الفصل 17 في كيفية مقارنة الأساليب في Rust بمبادئ البرمجة الموجهة نحو الكائنات التي قد تكون مألوفة لديك.

يعد الفصل 18 مرجعًا للأنماط وتطابق الأنماط، وهي طرق قوية للتعبير عن الأفكار في برامج Rust. يتضمن الفصل 19 مجموعة متنوعة من المواضيع المتقدمة المثيرة للاهتمام، بما في ذلك Rust غير الآمنة (unsafe Rust) والتعليمات البرمجية الموسعة (macros) والمزيد حول فترات الحياة والصفات والأنواع والوظائف والإغلاقات.

في الفصل 20، سنقوم بمشروع حيث سننفذ خادم ويب متعدد المواضيع على مستوى منخفض!

أخيرًا، تحتوي بعض الملاحق على معلومات مفيدة حول اللغة بتنسيق يشبه المرجع. تشمل الملحق A الكلمات الأساسية في Rust، والملحق B يغطي العوامل والرموز في Rust، والملحق C يغطي الصفات التي يمكن تشتيتها التي توفرها المكتبة القياسية، والملحق D يغطي بعض أدوات التطوير المفيدة، والملحق E يشرح إصدارات Rust. في الملحق F، يمكنك العثور على ترجمات للكتاب، وفي الملحق G سنتناول كيفية إنشاء Rust وما هو Rust الليلي (nightly Rust).

لا يوجد طريقة خاطئة لقراءة هذا الكتاب: إذا كنت ترغب في الانتقال إلى الأمام، فاذهب إلى ذلك! قد تحتاج إلى العودة إلى الفصول السابقة إذا واجهت أي ارتباك. سوف يساعدك Ferris أيضًا على التمييز بين الكود الذي لا يعمل:

| Ferris                                                                                                           | المعنى                                          |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <img src="img/ferris/does_not_compile.svg" class="ferris-explain" alt="Ferris with a question mark"/>            | هذا الكود لا يترجم!                      |
| <img src="img/ferris/panics.svg" class="ferris-explain" alt="Ferris throwing up their hands"/>                   | هذا الكود يؤدي إلى تعطل البرنامج!                                |
| <img src="img/ferris/not_desired_behavior.svg" class="ferris-explain" alt="Ferris with one claw up, shrugging"/> | هذا الكود لا ينتج السلوك المطلوب. |

في معظم الحالات، سنقودك إلى النسخة الصحيحة لأي كود لا يترجم.

## مصدر الشفرة

يمكن العثور على ملفات المصدر التي تم إنشاء هذا الكتاب منها على [GitHub][book].

[book]: https://github.com/rust-lang/book/tree/main/src