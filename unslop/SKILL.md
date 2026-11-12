---
name: unslop
description: Cuts AI writing tells from prose. Must always apply.
---

# Unslop

Edit text to remove AI patterns. Scan for the patterns below, then rewrite.
Preserve meaning and match the intended tone.

## Patterns to detect and fix

Rule numbers are stable ids that other skills cite. A removed rule leaves a gap.

### Content

3\. **Superficial -ing phrases.** "highlighting...", "ensuring...",
"reflecting...", "showcasing...", "fostering...". Delete or expand with real
sources.

5\. **Vague attributions.** "Experts believe", "Industry reports suggest", "Some
critics argue". Name the source or delete.

### Language

7\. **AI vocabulary.** Additionally, crucial, delve, enduring, enhance,
fostering, garner, interplay, intricate, landscape (abstract), pivotal,
showcase, tapestry (abstract), testament, underscore, vibrant. Replace with
plain words.

8\. **Fancy ways to say "is".** "serves as", "stands as", "boasts", "features".
Say "is" or "has".

9\. **"Not just X, but Y."** State the point directly instead.

10\. **Rule of three.** Don't force ideas into groups of three. Use the natural
number.

11\. **Synonym cycling.** Protagonist, main character, central figure, hero all
in one paragraph. Pick one, repeat it.

12\. **False ranges.** "from X to Y" where X and Y aren't on a meaningful scale.
List topics directly.

### Style

13\. **Em dash overuse.** Avoid em dashes entirely. Use periods or commas only
(no parentheses, no en dashes, no hyphen-as-dash substitutes). If a thought
needs separation, end the sentence or use a comma.

14\. **Colon overuse.** Colons are fine before a list or example, not as
mid-sentence connectors. "If you're coming from traditional automation: instead
of registering event handlers, you describe conditions" adds nothing with the
colon. Rewrite to let the point stand on its own without comparison framing.
"Describing when the scheduler should fire works best as plain English." Same
meaning, no crutch punctuation.

15\. **Boldface overuse.** Don't bold every proper noun or acronym.

16\. **Inline-header lists.** The tell is a bold label and colon that restates
the line: "**Performance:** Performance improved...". Convert those to prose. A
bold lead-in that ends in a period, names the item, and is followed by genuinely
new detail ("**Schema in TypeScript.** Tables live in one file.") is fine, not a
tell.

17\. **Title case headings.** Use sentence case.

18\. **Decorative emojis.** Remove from headings and bullets.

19\. **Curly quotes.** Use straight quotes.

### Communication artifacts

20\. **Chatbot phrases.** "I hope this helps!", "Let me know if...", "Of
course!", "Certainly!", "Found the smoking gun!" Remove.

22\. **Sycophantic tone.** "Great question! You're absolutely right!" Respond
directly.

### Filler

23\. **Filler phrases.** "In order to" becomes "To". "Due to the fact that"
becomes "Because". Delete "It is important to note that".

24\. **Excessive hedging.** "could potentially possibly be argued that it might"
becomes "may".

25\. **Generic conclusions.** "The future looks bright." State specific plans or
facts.

### Jargon

26\. **Abstract metaphor nouns.** Substrate (base), wedge, wedge in (add),
vector (way, method), locus, vantage, nexus, primitive as a noun, harness as a
metaphor, surface as in "API surface", bedrock, scaffolding as a metaphor,
modality, paradigm, gold-plating (more than the job needs), ratchet as a
metaphor (the mechanism's real name, or a limit that only tightens), evacuate
for moving code (move out), endgame (the last phase), north star, flywheel.
These read as technical but usually have a plainer concrete word. Pick the
concrete word.

### Plain speech

27\. **Say what it does, not how it feels.** "the database stays close at hand",
"SQL you can read", "types that follow your schema" name a feeling. The fix
names the mechanism or a number: "`.toSQL()` returns the exact string sent to
the database", "a column rename fails the build". Ask what the sentence tells
the reader to do or know, then write that. If you can't restate it as a concrete
instruction, fact, or number, cut it. One more check: if the sentence could
appear unchanged in another project's docs, it says nothing about this one. Cut
it.

28\. **Shorten or split dense sentences.** If the reader has to backtrack to
parse a sentence, break it in two or drop clauses. One idea per sentence.

29\. **Active voice.** Prefer it. Catch "is/are/was/were + past participle" and
name the actor: "queries are validated" becomes "the compiler validates
queries", "the file is parsed by the loader" becomes "the loader parses the
file". Passive is fine only when the actor is unknown or genuinely doesn't
matter.

30\. **Cut adverbs, or use a stronger verb.** "runs quickly" becomes "is fast"
or the number, and "significantly improves" becomes the measured delta. An
adverb propping up a weak verb means the verb is wrong.

31\. **Prefer the plain word.** "utilize" and "leverage" become "use",
"facilitate" becomes "help", "numerous" becomes "many", "in the event that"
becomes "if". The fancier synonym is rarely clearer.

33\. **Over-compression.** Dropped articles, verbless fragments, symbol-speak,
and abbreviations that make the reader decode instead of read. "Parser rejects
bad date → exit 2, no write" becomes "The parser rejects a bad date, exits with
code 2, and writes nothing." Write whole sentences with their articles and
verbs, and spell out arrows and abbreviations.

### Mannered prose

> [!NOTE]
> This tell survives every other fix in this list because it reads as skill
> rather than slop. Scrub the earlier rules first, then check for what is
> left. Rule 26 covers the metaphor nouns.

34\. **Metaphor swaps.** Swapping the literal phrase for a metaphor or flourish
so the sentence can perform good writing: "a dial worth turning" becomes "a
parameter worth varying", "this point earns its keep" becomes "this point still
matters", "load-bearing" becomes "required". The phrases exist to display the
writer, not to convey the idea, and readers can tell. Say what you mean. When a
literal phrase is available, use it.

35\. **Stray connotations.** Metaphors drag in connotations nobody chose: "a
dial" imports analog and adjustable where the thing is a boolean. Ask what the
figure implies that the plain phrase does not.

36\. **Inanimate subjects.** Objects given feelings or figurative verbs to earn
a clever turn: "the index knows nothing of user patience", "the plan holds it",
"this function rides along". Name the mechanism instead.

37\. **Orbiting sentences.** Sentences that circle a point through clause after
clause, then land it like a revealed insight. Lead with the point.

38\. **Wistful codas.** Philosophical sign-offs bolted onto technical text: "in
the end, software is about the quiet promises systems make". Cut the coda; the
instructions before it are the content.

46\. **Aphorisms.** Stock dictums standing in for guidance: "wire it or delete
it". Say the actual rule for the case at hand.

### Performative wording

> [!NOTE]
> Unlike mannered prose there is no metaphor to swap out. Delete the whole
> run-up, not just its tone: "And honestly? Here's the thing: it fails under
> high concurrency" becomes "It fails under high concurrency".

39\. **Performed candor.** Announcing honesty before a routine claim: "I'll be
blunt:", "not going to lie", "let's be honest". Make the point directly.

40\. **Staged revelation.** Dramatic run-ups that fake suspense: "Here's the
thing:", "And honestly?". The claim that follows is usually ordinary. Cut the
run-up.

41\. **Audience directions.** Commands telling the reader when to react: "Let
that sink in", "Sit with that", "Read that again". Remove them.

42\. **Announced emotion.** Telling the reader how to feel instead of showing
what earned the feeling: "quietly devastating", "genuinely fascinating",
"chillingly simple". Describe the thing.

43\. **Self-narration.** Reporting the text's own effect on the writer: "this
one hit me", "I keep coming back to this". State the idea. Cut the reaction
report.

44\. **Ghost objections.** Arguing with objections nobody raised: "To be clear,
I'm not saying...", "Don't get me wrong". Answer the actual point.

45\. **Typographic drama.** Formatting doing the emphasis work: italics on
*actually*, "Every. Single. Day.", one-word paragraphs. Write the sentence so it
needs none.
