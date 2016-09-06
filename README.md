#Vergil Quiz Generator

I built this in response to a request from a friend.

##User Persona
Janet (not her real name) is a lecturer who teaches Latin at the college level. One of the staples of Latin is reading Vergil's poem, the **Aeneid**, and traditionally most two-year Latin curricula include a whole course devoted to that. Quizzes are a good way to make sure students are keeping up. If Janet uses the same passages over and over, it's tempting for students to memorize the passage instead of actually translating it. So Janet spends a lot of time choosing and copying passages, a task further complicated by the tedium of either a) copying manually from the text (remember photocopiers?) or b) trying to use online sources, which may have formatting problems and differences.

##User Story
As Janet, I'd like a way to make quizzes quickly, so that I don't waste time with copying and pasting. I'd like the default to be random, so that students won't be able to cheat, but it would be great if I could choose the passage and book when needed, because I occasionally have something in mind.

##Tech
There's a great [Vergil API](http://aeneid.eu/api/) available online, so that part was easy.

This was also a chance to revisit one of my favorite topics, namely, poetic HTML semantics -- and yes, there's a [WC3 discussion](https://www.w3.org/html/wg/wiki/PoeticSemantics) for that! I went with with dd elements in order to avoid the autoformatting that comes with li elements; also, there's something that philosophically bothers me about treating poems as lists.

When I built this, I originally envisioned it as a one-page app. After getting the basic functionality in place, I decided to use a CSS framework to make it look better and work across devices and as the JS gets more complex I'll probably break that out too. I also used it as an opportunity to explore the cool new features in [HTML5 form validation](http://www.html5rocks.com/en/tutorials/forms/html5forms/).

#TODOs
1. The API doesn't currently allow multiple lines to be grabbed with a book or line parameter; until it does, the generator will have to be entirely random.
2. Beginning Latin instructors often help their students with meter by showing long and short marks on the text; the API won't do that, but there is a Python classical languages toolkit that might. Then again, that would mean re-building this in Python...
