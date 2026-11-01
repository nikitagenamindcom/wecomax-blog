# An assistant that keeps answering when its suppliers have a bad day

*1 November 2026*

The worst failure in a small business is rarely a slow answer. It is no answer at all: a client writes, something behind your assistant has a bad hour, and the message sits there until the client goes to the next shop.

Tonight we shipped a set of changes with one goal — **an answer always arrives.**

**If one supplier fails, the next one answers.** Callbot does not depend on a single AI provider. When a request fails or gets refused, it is quietly handed to the next one, and the client sees only an answer. A supplier that keeps failing drops to the back of the queue by itself, so their bad hour does not become your bad hour.

**The assistant checks itself.** Every few minutes Callbot tests what it depends on: the models, search, pictures, the live link between your phone and your computer, and the machine's own disk. If something breaks, you are told in plain language — before your clients tell you. It costs about two cents a day to run.

**Search answers in about three seconds.** Lookups and translations now take the fast path, so a simple question from your phone does not feel like a project.

**An honest timer.** When you ask something from your phone, the «Working… 12 s» line used to restart at every step of the job. Now it counts the whole answer from start to finish. Small thing, but the number you see is the time you actually waited.

What we learned building it:

1. **Reliability is a feature, not a hygiene factor.** Owners never praise it, and they leave when it is missing.
2. **A good-enough answer now beats a perfect one later.** Three seconds wins the client; an hour loses them.
3. **Measure, do not hope.** A tool that checks itself and reports what broke saves more evenings than the monitoring dashboard you meant to set up someday.
4. **Say what really happened.** If a timer, a status or a promise shows something that is not true, people stop trusting everything else on the screen — including the parts that work.

**One practical tip you can use today:** take the single thing your business depends on most — the messenger your clients write in, the payment link, the one phone that holds all the contacts — and write a one-line backup for it. Where does the same thing happen if it dies for a day? Then test that line once this week, for ten minutes. Most owners discover the backup only existed in their head.

Callbot by Wecomax keeps answering your clients on your own computer, in their language, with the boring reliability work already done: [callbot.wecomax.com](https://callbot.wecomax.com).

— Anna, Marketing at Wecomax
