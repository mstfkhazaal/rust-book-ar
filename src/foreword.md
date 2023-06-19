# Foreword

It wasn’t always so clear, but the Rust programming language is fundamentally
about *empowerment*: no matter what kind of code you are writing now, Rust
empowers you to reach farther, to program with confidence in a wider variety of
domains than you did before.

Take, for example, “systems-level” work that deals with low-level details of
memory management, data representation, and concurrency. Traditionally, this
realm of programming is seen as arcane, accessible only to a select few who
have devoted the necessary years learning to avoid its infamous pitfalls. And
even those who practice it do so with caution, lest their code be open to
exploits, crashes, or corruption.

Rust breaks down these barriers by eliminating the old pitfalls and providing a
friendly, polished set of tools to help you along the way. Programmers who need
to “dip down” into lower-level control can do so with Rust, without taking on
the customary risk of crashes or security holes, and without having to learn
the fine points of a fickle toolchain. Better yet, the language is designed to
guide you naturally towards reliable code that is efficient in terms of speed
and memory usage.

Programmers who are already working with low-level code can use Rust to raise
their ambitions. For example, introducing parallelism in Rust is a relatively
low-risk operation: the compiler will catch the classical mistakes for you. And
you can tackle more aggressive optimizations in your code with the confidence
that you won’t accidentally introduce crashes or vulnerabilities.

But Rust isn’t limited to low-level systems programming. It’s expressive and
ergonomic enough to make CLI apps, web servers, and many other kinds of code
quite pleasant to write — you’ll find simple examples of both later in the
book. Working with Rust allows you to build skills that transfer from one
domain to another; you can learn Rust by writing a web app, then apply those
same skills to target your Raspberry Pi.

This book fully embraces the potential of Rust to empower its users. It’s a
friendly and approachable text intended to help you level up not just your
knowledge of Rust, but also your reach and confidence as a programmer in
general. So dive in, get ready to learn—and welcome to the Rust community!

— Nicholas Matsakis and Aaron Turon
## مقدمة

لم يكن الأمر دائمًا واضحًا، ولكن لغة برمجة Rust في جوهرها تعتمد على *تمكينك*: بغض النظر عن نوع الشيفرة التي تقوم بكتابتها الآن، فإن Rust يمكنك من الوصول إلى أبعد من ذلك، وبرمجة بثقة في مجموعة أوسع من المجالات مما كنت تفعله في السابق.

لنأخذ على سبيل المثال العمل "على مستوى النظام" الذي يتعامل مع تفاصيل منخفضة المستوى لإدارة الذاكرة وتمثيل البيانات والتوازي. تقليديًا، يُعتبر هذا المجال من البرمجة صعبًا ويمكن الوصول إليه فقط من قبل القلة المنتخبة الذين قدموا سنوات طويلة في تعلم كيفية تجنب الأخطاء المشهورة بها. وحتى أولئك الذين يمارسونه بحذر، يخشون أن يكون لديهم شيفرة مفتوحة للاستغلال أو الانهيارات أو التلف.

تُحطم Rust هذه الحواجز من خلال القضاء على المشاكل القديمة وتوفير مجموعة من الأدوات الودية والمنتهية التنقيح لمساعدتك في سير العمل. يمكن للمبرمجين الذين يحتاجون إلى "التغوص" في التحكم على مستوى أقل القيام بذلك باستخدام Rust، دون تحمل المخاطر التقليدية للاستنهاض أو الثغرات الأمنية، ودون الحاجة إلى تعلم تفاصيل دقيقة عن سلسلة أدوات متقلبة. والأهم من ذلك، تم تصميم اللغة لتوجيهك بشكل طبيعي نحو كتابة شيفرة موثوقة تكون كفوءة من حيث السرعة واستخدام الذاكرة.يمكن للمبرمجين الذين يعملون بال

فعل بشيفرة منخفضة المستوى استخدام Rust لرفع طموحاتهم. على سبيل المثال، يعتبر إدخال التوازي في Rust عملية ذات مخاطر منخفضة نسبيًا: سيتعرف المُترجم على الأخطاء التقليدية بالنسبة لك. ويمكنك التعامل مع المزيد من التحسينات الهجومية في شيفرتك بثقة بحيث لا تقوم عن طريق الخطأ بإدخال الاستنهاض أو الثغرات.

ولكن Rust ليست مقتصرة على برمجة أنظمة منخفضة المستوى. إنها قوية ومريحة بما يكفي لجعل تطبيقات سطر الأوامر وخوادم الويب والعديد من أنواع الشيفرة الأخرى ممتعة للكتابة - ستجد أمثلة بسيطة على كل منها في وقت لاحق في الكتاب. العمل مع Rust يسمح لك ببناء مهارات تنتقل من مجال إلى آخر؛ يمكنك تعلم Rust من خلال كتابة تطبيق ويب، ثم تطبيق نفس المهارات لاستهداف Raspberry Pi الخاص بك.

يتبنى هذا الكتاب بشكل كامل إمكانات Rust لتمكين مستخدميها. إنه نص ودي ومفهوم يهدف إلى مساعدتك على رفع مستوى معرفتك بـ Rust، وكذلك مدى تأثيرك وثقتك كمبرمج عمومًا. لذا اغمر فيه، واستعد للتعلم - ومرحبًا بك في مجتمع Rust!

- نيكولاس ماتساكيس وآرون تورون