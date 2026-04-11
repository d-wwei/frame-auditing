# Frame Auditing — Before/After Examples

Four scenarios across different domains, demonstrating the cognitive protocol in action.

---

## Example 1: Engineering

**User**: "This code is too complex to maintain. Should we refactor or rewrite?"

### Before (default mode)

> Here's how to decide between refactor and rewrite:
>
> **Refactor if**: the code works, the test coverage is decent, and the complexity is localized.
> **Rewrite if**: the architecture is fundamentally wrong, tech debt is pervasive, and the team is spending more time fighting the code than building features.
>
> Based on industry data, rewrites typically take 2-3x longer than estimated, so I'd lean toward incremental refactoring with the Strangler Fig pattern unless the codebase is truly unsalvageable.

**Problems**: Accepts the "too complex" frame without questioning it (frame blindness). "Too complex" is an encoding that has already judged the code — but complex for whom? For the original authors, or for the current team who didn't write it? (encoding blindness). The refactor/rewrite dichotomy is itself a frame that excludes other possibilities.

### After (cognitive protocol active)

> "Too complex to maintain" embeds two judgments worth examining.
>
> First, "complex" — compared to what baseline? If the original team maintained it fine and your current team can't, the problem might be **knowledge loss**, not code quality. The fix for a knowledge problem is documentation and pairing sessions, not refactoring.
>
> Second, "to maintain" — what specific maintenance tasks are failing? If deployments are slow, that's a build/deploy pipeline problem. If bugs are hard to trace, that could be a logging/observability problem. If new features are slow to add, identify whether it's coupling (architecture) or comprehension (knowledge).
>
> The refactor/rewrite frame assumes the code itself is the problem. But code doesn't become "too complex" — it becomes too complex *for a specific team in a specific context*. Before touching the code, identify whether you have a code problem, a knowledge problem, or a tooling problem. Each has a different solution, and only one of them is refactoring.

**Active shifts**: Frame detection — named the "code is the problem" frame and identified alternatives (knowledge problem, tooling problem). Encoding audit — unpacked the judgments embedded in "too complex." Attribution check — the code didn't change; something about the team or context did.

---

## Example 2: Business

**User**: "Our competitor is winning on price. How should we respond?"

### Before (default mode)

> Here are five strategies for competing on price:
>
> 1. Reduce costs through supply chain optimization
> 2. Offer tiered pricing with a competitive entry point
> 3. Bundle features to increase perceived value
> 4. Target a premium segment that's less price-sensitive
> 5. Match their price on your most popular plan and make it up on upsells
>
> The best approach depends on your cost structure and customer segment. I'd recommend starting with a competitive analysis to understand their cost advantages.

**Problems**: Accepts "winning on price" as the frame without checking whether price is actually the decision factor (frame blindness). All five strategies assume the price frame is correct. "Competitive analysis" is jargon that sounds actionable but specifies nothing concrete (form without content).

### After (cognitive protocol active)

> "Winning on price" is a frame. Let me check whether it fits the data.
>
> What does your churn data actually say? If exit surveys cite price, note that customers post-rationalize with the most socially acceptable reason. If they're switching to a product with fewer features at a lower price, they're telling you they don't use — or don't value — the features you charge for. That's a value-fit problem, not a price problem.
>
> Check: are you losing new prospects (they compare and choose the competitor) or existing customers (they switch after using your product)? If new prospects — your positioning might be failing to communicate value before the price comparison happens. If existing customers — they've experienced your product and decided it's not worth the delta. These require completely different responses.
>
> The price frame says "reduce costs or increase perceived value." The value-fit frame says "understand which features actually drive purchasing decisions and double down on those." The positioning frame says "change how prospects encounter the comparison." Competing on price when the actual problem is value-fit or positioning will erode margins without solving the real issue.
>
> Stage check (初级阶段论): if you're still discovering which features drive retention, you're in exploration stage — running pricing experiments now is premature optimization.

**Active shifts**: Frame detection — named "price competition" as a frame and proposed alternatives (value-fit, positioning). Encoding audit — "winning on price" presupposes price is the battlefield. Attribution check (反求诸己) — checked internal factors (value communication, feature-value alignment) before responding to external competitor. Stage calibration — flagged that pricing strategy requires product-market fit first.

---

## Example 3: Personal

**User**: "I don't have enough time for strategic work. I'm stuck in meetings and firefighting all day."

### Before (default mode)

> This is a common challenge for leaders. Here are some strategies:
>
> 1. Block 2-3 hours of "deep work" time on your calendar
> 2. Delegate more operational decisions to your team
> 3. Implement a meeting audit — cancel any meeting without a clear agenda
> 4. Use the Eisenhower Matrix to prioritize important over urgent
> 5. Set up office hours instead of ad-hoc availability
>
> The key is protecting your strategic time. Consider starting with one "no-meeting day" per week.

**Problems**: Accepts the "not enough time" frame as reality (frame blindness). "I don't have enough time" is an encoding that externalizes the cause — time is the problem, not my choices (attribution externalization). All advice is time-management, but the issue might not be time at all.

### After (cognitive protocol active)

> "I don't have enough time" is a universal complaint, which is exactly why it's worth auditing. Time is fixed; the question is what fills it.
>
> Attribution check (反求诸己): you say you're "stuck in" meetings and firefighting, framing them as things that happen to you. But: who accepted those meeting invites? Who trained the team to escalate to you instead of deciding themselves? The firefighting frame says "emergencies keep appearing." The leadership frame says "I haven't built systems that prevent or handle emergencies without me."
>
> Encoding audit: "strategic work" vs "meetings and firefighting" encodes one as valuable and the other as waste. But some meetings ARE your strategic work — alignment, decision-making, information flow. The problem isn't meetings; it's that you haven't classified which meetings are strategic and which are habitual.
>
> The real question isn't "how do I find more time?" It's one of:
> - **Delegation gap**: Have I equipped my team to make decisions I'm currently making?
> - **System gap**: Do my processes prevent fires, or am I the fire department?
> - **Clarity gap**: Do I actually know what "strategic work" means concretely, or is it an aspirational label for "things I'd rather be doing"?
>
> Time management advice treats the symptom. The frame to examine is: why does your role require you in the loop for so many things? That's a system design problem, not a scheduling problem.

**Active shifts**: Frame detection — shifted from "time scarcity" frame to "system design" frame. Attribution check (反求诸己) — reattributed from external ("meetings happen to me") to internal ("I accept/create the conditions"). Encoding audit — challenged the value judgment embedded in "strategic work" vs "firefighting." Stage calibration — identified that the root issue (delegation and system design) must be solved before time management tools are useful.

---

## Example 4: Communication

**User**: "The team doesn't understand the strategy. I've explained it three times already."

### Before (default mode)

> Communication failures usually come down to clarity and repetition. Here's what I'd suggest:
>
> 1. Simplify the strategy to 3 key pillars they can remember
> 2. Create a one-page visual summary
> 3. Use multiple channels: all-hands, Slack, 1:1s, written docs
> 4. Ask each team lead to explain it back to you in their own words
> 5. Tie daily work to the strategy explicitly ("This sprint we're working on Pillar 2")
>
> Research shows people need to hear something 7-10 times before it sticks. Keep at it.

**Problems**: Accepts the frame that the team has a comprehension problem (frame blindness). "I've explained it three times" attributes the cause entirely to the receivers — they don't understand (attribution externalization). "Explained" encodes the communication as adequate by definition (encoding blindness). The advice is all about how to transmit harder, not about whether the message is receivable.

### After (cognitive protocol active)

> "The team doesn't understand" places the failure on the receiving end. Let me check that frame.
>
> Attribution check (反求诸己): you've explained it three times. After three explanations, if a roomful of intelligent people still "don't understand," the hypothesis "they're bad at listening" is less likely than "the explanation has a problem." What problem?
>
> Possibilities the current frame hides:
> - **The strategy contradicts their incentives.** They understand it fine but see that executing it conflicts with how they're measured. "Not understanding" is polite resistance.
> - **The strategy is abstract.** You've communicated the destination but not the first step. They can repeat "we're going to be customer-centric" but can't translate it into Monday's work.
> - **The strategy changed but the narrative didn't.** If this is the third version, "I don't understand" might mean "I don't trust this one to stick."
>
> Encoding audit (春秋笔法): "explained" presupposes that what you said was clear and complete. But explanation is defined by the receiver's comprehension, not the sender's effort. Reframe: "I've transmitted the strategy three times and it hasn't landed." That framing opens you to examining your transmission, not just their reception.
>
> Perspective switch (Inamori): from the team's position, they see a leader who keeps saying the same thing with increasing frustration. That pattern signals "agree or be seen as not getting it" — which shuts down the questions that would actually build understanding.
>
> Before explaining a fourth time: ask three team members what they think the strategy is and why. The gap between their version and yours is the actual problem to solve — and it might reveal that the strategy itself is unclear, not just the communication.

**Active shifts**: Frame detection — shifted from "team comprehension" frame to "communication design" and "incentive alignment" frames. Attribution check (反求诸己) — redirected from receiver's failure to sender's contribution. Encoding audit (春秋笔法) — unpacked "explained" as encoding that pre-exonerates the sender. Perspective switch (Inamori) — viewed from the team's position to reveal how the repetition pattern itself is counterproductive.
