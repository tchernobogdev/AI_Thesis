# Are We in a Bubble?

## The Bull Case

Before getting into the bear case, it is worth laying out the best arguments for the AI trade and against the bubble theory:

- P/E ratios are somewhat reasonable and far below what they reached during the dot-com bubble.
- Earnings for semiconductor companies, the main initial beneficiaries of the AI trade, are still growing QoQ and YoY at unprecedented scales and rates.
- AI companies like OpenAI grew their extremely large user bases at the fastest rate of any service provider in history.
- Sophisticated investors across the board are all in on AI, and private funding rounds for AI companies have reached valuations nearing $1 trillion.
- AI productivity gains will result in faster economic growth.
- Unit economics on price per million tokens are improving.
- Falling inference costs could cause usage to explode, meaning total demand for compute could keep increasing even if each individual token becomes cheaper.
- AI could become a monetization layer inside existing software, advertising, commerce, cloud, and enterprise workflows instead of needing to be justified entirely through chatbot subscriptions.
- Governments may eventually treat AI infrastructure as a strategic necessity, not just a normal private-sector ROI calculation.

That is the best version of the bull case, in my view. The problem is not that these arguments are stupid. They are not. The problem is that almost all of them still eventually run into the same question: where does the return on all of this spending actually come from? Lower costs, higher usage, enterprise adoption, ads, commerce, and government support can all help, but none of them remove the need for someone to eventually earn a return on the capex. They only change where the return is supposed to show up.

## The Bear Case

The other side of the trade is that the scale of spending has started to look impossible to justify through normal business returns:

- Capex is increasing to a level that makes getting a return on investment impossible.
- Circular financing and revenue quality issues.
- Concentration risk.
- GPU depreciation understatements.
- Market euphoria amid rising economic strain and geopolitical conflicts.

Let’s be honest: there are teams of Chinese quants with a dozen math olympiad gold medalists performing incomprehensible analyses that are far beyond what any individual trader can hope to imitate, so there is essentially no point in trying. For this analysis, I want to take a more intuitive and holistic approach to the AI trade and my thoughts on the bull vs. bear arguments.

The cleanest way to start is to follow the money.

## Following the Money

The majority of AI-related spending is flowing into semi and memory companies at the moment. NVDA reported Q1 FY2027 revenue of $81.6 billion, up 85% from a year ago, and Non-GAAP EPS of $1.87, making it a double beat on analyst expectations. They also raised their Q2 guidance to $91 billion, up from the consensus estimate of $87.2 billion. Never in history has a company of this size posted such incredible revenue and earnings growth.

The vast majority of this incredible revenue comes from the spending of hyperscalers and the two AI model favorites, OpenAI and Anthropic. Everyone understands that when a company spends money, it is not for charity. They expect to get a return on that spending. Hyperscalers have the pre-established cash flow and deep cash reserves to spend their own money, but OpenAI and Anthropic are not hyperscalers and are far from profitability.

That is where the trade starts to get more interesting. The companies driving a major portion of demand are not necessarily the same companies with the cleanest path to profitability.

The bull response here is that hyperscalers can afford it. That is true, but it is also not the same thing as proving the spend is rational. MSFT, AMZN, GOOG, and META can all light tens of billions of dollars on fire and still survive. That does not mean investors will be happy if the money fails to generate returns above their cost of capital. The question is not whether these companies can fund the buildout. They can. The question is whether the buildout produces enough future cash flow to justify the amount of money being spent now.

## OpenAI as the Case Study

OpenAI has been the favorite in the AI model race for most of the AI trade, with Anthropic arguably taking the lead for a short time before Codex 5.5 was released by OpenAI. For that reason, I will use OpenAI as the case study here.

To be clear, OpenAI is not the entire AI market. Google is structurally different because it has search, ads, cloud, TPUs, Android, YouTube, Workspace, distribution, and massive existing cash flow. Microsoft, Amazon, and Meta are also not the same as OpenAI. However, OpenAI is the cleanest case study for the independent frontier model company. It has the users, the brand, the enterprise demand, the valuation, and the compute obligations. If the gold standard independent model company has a difficult path to profitability, then it is at least worth asking what that says about the rest of the model-company layer.

OpenAI is valued somewhere in the range of $900 billion, with reported annual revenue of $25B and cash burn of $27B, implying estimated spend of $52B. However, that $25B revenue figure is rumored to simply be their most recent four weeks of revenue multiplied by 13. These figures are also not audited and partially come from leaks, which means they need to be taken with a grain of salt. However, it is confirmed that OpenAI has $600B of take-or-pay spending obligations through 2030. So, for future napkin math, let’s give OpenAI the benefit of the doubt on its $25B revenue figure, but use its actual spending obligations, in addition to current spend, as part of a payment schedule through 2030.

There is also a small but important accounting-quality point here. When a market gets this hot and the same handful of companies are investing in each other, buying from each other, renting to each other, and using those deals to justify the next valuation mark, the reported revenue number becomes less clean than it looks at first glance. I am not saying it is fake. I am saying that if part of the demand is being supported by vendor financing, equity investments, take-or-pay commitments, preferred pricing, or strategic partnerships that would not exist in a normal market, then the revenue is more fragile than a normal SaaS revenue line. It can look recurring right up until the capital cycle stops recurring.

Looking purely at spend here, instead of cash burn, which needs to account for revenue, a fair napkin math estimate would be:

- 2026: $70B
- 2027: $135B
- 2028: $190B
- 2029: $210B
- 2030: $200B, with the Stargate buildout finished

Now that we have the spending estimate for one of Nvidia’s largest end customers, meaning compute purchasers/renters, the next step is to look more closely at its business model and path to profitability.

## The User Model Problem

OpenAI claims to have 900M active weekly users. However, only ~5.5% of those users pay for the service, a total of about 50M paid users. The current plans offered by OpenAI are API usage, which is token based, Free, Go ($8/mo), Plus ($20/mo), Pro 5x ($100/mo), and Pro 20x ($200/mo). According to Sacra, OpenAI had inference costs, or CoGS, of $8.4B.

Based on API token usage, it is estimated that a Pro 20x user could cost OpenAI upwards of $2,000 a month in inference costs if they fully utilize their subscription. Of course, most users are unable to fully utilize their subscription, which results in some level of subsidization of power users. It also explains why on-demand usage via API tokens tends to be 10-20x more expensive than subscription plans. Note that inference costs here mostly refer to money paid to Oracle and MSFT for renting compute, which we can assume is being rented to OpenAI at a steep discount compared to what a regular person would pay.

Based on that, it is fair to estimate, conservatively, that users, even at lower subscription tiers, are costing OpenAI more than the amount of their subscription, up to 20x the subscription cost at the highest usage tiers for power users.

This is the first major issue with the AI trade: massive user growth does not automatically mean profitable user growth.

## What It Costs to Run These Models

To further back up this claim, let’s look at what it would cost if you wanted to host a model of comparable size to GPT 5.5 or Opus 4.7, which are estimated to be in the 5 trillion parameter range. At a precision of FP16 for 5.5 trillion parameters, the total model weights to be loaded into memory, including overhead, would be somewhere in the range of 12TB. Using B200 SXM GPUs, which have 192GB of VRAM, you would need ~64 B200 GPUs to run just a single instance of one of these models for personal inference. Training, which needs to store additional optimizer states, would require upwards of 70TB of VRAM.

I have personally trained models from scratch, both LLMs and diffusion models, and even then, the GPU rental for simple 4B parameter models ran me over $5,000 in a single month. For a model at 5T parameters, using 64 B200 GPUs at the Runpod rental fee of $4.99/hr, it would cost $233k per month to host the model for personal inference. Of course, OpenAI is serving its model to multiple users, which allows it to save costs through concurrency. That is nearly impossible to estimate, but I just wanted to provide a rough idea of what it would cost a regular individual to rent the compute to run just a single instance of these models.

Given the rough napkin math, OpenAI needs to increase its annual revenue to around $200B by 2030 to have its first profitable year, all while fighting against inference unit economics and datacenter component prices.

At this point, the obvious bull response is that costs will come down. That is probably true. The problem is what happens to the rest of the AI trade if they come down too quickly.

## The Inference Cost Counterargument

The main bull counterpoint is that inference costs will decrease as GPU and LLM architecture continues to improve. The better version of this argument is that cheaper inference will not reduce GPU demand, but increase it. If tokens get 10x cheaper, then AI can be put into every search bar, spreadsheet, IDE, CRM, customer-service workflow, enterprise dashboard, phone, laptop, and toaster with WiFi. This is the Jevons paradox argument, and it is probably the strongest bull case against the cost side of my thesis.

However, cheaper usage does not automatically mean better returns. If inference costs fall and usage explodes, the relevant question is whether monetization grows faster than usage. If AI companies serve 10x more tokens at 1/10th the cost, but revenue per unit of usage collapses at the same time, then demand can explode while returns on capital still disappoint. Growth is not the same thing as profitable growth, which is exactly the point of this whole writeup.

There is also an internal contradiction in the bull case. The model companies need compute to get much cheaper so their margins can eventually work. But semiconductor and datacenter investors need compute demand and pricing to stay strong enough to justify the buildout. If new GPUs or new architectures make inference dramatically cheaper, they help the model labs, but they also speed up the economic obsolescence of older GPU fleets. If a Pro 20x user can cost OpenAI many times more than they pay in subscription fees, inference costs may need to fall by an order of magnitude just to make that tier rational. But if that happens because new hardware is that much better, why would older hardware retain anywhere close to its current economics?

Let’s say GPU technology improves rapidly and makes inference and training compute costs much less of an issue. What happens to the older GPUs? If the unit economics of newer GPUs are so attractive that they solve the inference and training cost problem, it only speeds up the depreciation of previous GPU generations, a point brought up by Michael Burry.

Let’s say LLM architecture improves and reduces inference needs. That helps OpenAI’s margins, but it also reduces the amount of compute required per unit of output. Bulls can argue that demand will expand enough to offset this, and maybe it will. But that means the entire infrastructure trade depends on demand increasing faster than efficiency improves. That is possible, but it is not guaranteed. If demand does not expand fast enough, datacenter investors lose from excess compute supply, semiconductor investors lose from lower forward demand, and model companies still need to prove they can monetize the usage they already have.

So is that it? Not quite. This all assumes that OpenAI derives its revenue primarily from individual users, but OpenAI has already been reported to attribute 40% of its revenue to enterprise deals, so let’s take a look at that next.

## The Enterprise Model

If the path to profitability doesn’t exist for a user-centric model, what happens in the case of an enterprise-centric model? Let’s keep it simple this time and look across the board at AI spend, which I will estimate to follow this payment schedule at current trajectories:

- 2026: $635B
- 2027: $815B
- 2028: $970B
- 2029: $1.1T
- 2030: $1.15T

Note that these are extremely rough estimates based on MSFT, AMZN, GOOG, META, ORCL, and OpenAI spending.

The bull response is that AI does not need to be profitable through OpenAI subscriptions because it can be monetized through enterprise software, cloud, advertising, commerce, agents, APIs, and workflow automation. That is fair, but it does not solve the problem. It just moves the problem. Advertising only works if advertisers see incremental revenue, commerce only works if merchants make more money or give up margin, enterprise software only works if companies get measurable ROI, and cloud only works if customers are willing to keep paying for the compute. Every path still eventually runs into the same wall: someone needs to make more money, save more money, or pass the cost along to somebody else.

Taking the 2027 number and making it an even $800B for now as our base for this napkin math, let’s look at how enterprise deals alone would justify AI spending. First, we need to know how many workers AI could “increase productivity” for. Let’s assume that 40% of ChatGPT’s paid users are in the US. There are roughly 100M white collar workers in the US, so let’s say the global OpenAI white collar worker TAM is 250M white collar workers (100M / 0.4).

Why white collar workers? Well, AI and robotics are far from replacing waitresses, mechanics, janitors, electricians, and strippers. It primarily targets desk jobs. The median white collar salary in the US is ~$65k. The reason I am getting all these numbers ready is because, despite what hedge fund managers, tech company CEOs, economists, and researchers might tell you, AI is not here to just increase all worker productivity across the board.

The enterprise bull case is usually framed as a productivity story. My view is that, in practice, it eventually becomes a cost-cutting story.

This is also where the “OpenAI is not the whole market” counterargument stops mattering as much. I agree that OpenAI is not the whole market. But the AI trade still relies on model companies and hyperscalers eventually justifying the infrastructure spend. If the justification is enterprise adoption, then enterprise customers need to get returns from the tools. If those returns are not coming from new consumer demand, then they have to come from margin expansion, and the cleanest form of margin expansion is labor cost reduction.

## Productivity Gains or Cost Cutting?

First, a tangent to explain my view here. There is only so much work to be done. If Ford were to double the number of cars it produces in a year, or Netflix were to triple the amount of code written in a year, or Apple were to produce three times as many iPhones, even at zero additional cost, it would not meaningfully increase their revenue because the market is already saturated. In situations where there is far more demand than supply, the supply is gated by physical resources, fabrication allocations, or human time to produce, mainly referring to physical labor, such as artisan chairmaking and similar situations.

So, if AI were to triple the productivity of 250 million white collar workers, where does all of that productivity go? Currently, it goes into more free time for workers! There is currently a corporate worker golden age, especially for remote or hybrid workers, where the productivity gains from effective AI tool use just reduce how much time workers need to spend working to exceed the expectations of their role.

However, corporations are slow, not stupid (maybe a little stupid). Eventually, middle and upper management are going to take a look at the “productivity gains” of their AI adoption and the amount they are spending on AI, then all come to the same conclusion: “We can have half the workers complete twice as much work,” or some variation of that. This means that for corporations to justify AI tooling spend, it is through the lens of cost cutting, not increasing revenue through productivity gains.

The bull case can point to fewer errors, better customer service, faster sales cycles, better coding output, better internal tools, and a hundred other marginal improvements. I am not saying those are fake. They are real. The problem is that marginal improvements do not obviously pay back hundreds of billions of dollars in annual AI spend across the economy. For a single company, maybe the ROI works. Across the whole system, the money still has to come from somewhere. Either final demand increases, margins increase, labor costs fall, or another sector eats the cost. Given the current macro backdrop, I have a hard time seeing final consumer demand magically growing enough to make the numbers work.

That is where the enterprise bull case starts to turn into a macro problem.

## The Job Displacement Problem

Just to briefly cover a counterpoint: some might argue that, like previous technological revolutions, jobs will also be created to offset the job losses. However, AI has the highest “backend” skillset requirement of any technology in history. For instance, the internet created IT jobs, networking jobs, software jobs, etc., all of which had requirements at or below a bachelor’s degree. AI would create jobs for data scientists, architecture researchers, chip designers, etc., all of which are, at minimum, master’s degree-level roles. Even then, if you look at the hiring of companies like OpenAI and Anthropic and specifically look for roles that AI has essentially created a demand for, they are almost all PhD-level roles.

Going back to the napkin math of 250M white collar workers, who make a median of ~$65k, and the AI spend that needs to be recouped for 2027 of ~$800B: companies would need to cut ~$800B worth of costs, meaning jobs, which comes out to ~12.3 million jobs. If we apply the 40% of paid users for OpenAI in the US to the 12.3 million, we get ~5 million jobs that would need to be cut in the US alone.

These estimate figures are extremely generous on all sides. They are generous on the total AI spend side. They are generous on the total jobs attributable to enterprise AI deal replacement side, as the vast majority of large companies that would sign enterprise deals are in the US. They are also generous on the cost-cutting side, since most companies signing enterprise deals have a responsibility to shareholders to cut as many jobs as possible. So if AI is a 5x productivity gain, they aren’t going to just cut enough workers to break even with the enterprise deal costs.

Assuming 5 million white collar jobs were lost, which I consider a very conservative estimate, that would increase U-3 unemployment to ~7.3%. Add on top of that the highest cost-of-living to median-wage ratio in the last 50 years, likely more, and the likelihood that most of the people who lose their jobs will then be stuck in a job market where the trend is cutting costs in their field. These former workers will then be forced into the gig economy, minimum wage jobs, lower salary positions, or just remain unemployed. People under 30 already well understand the true state of the economy at the present, which makes supporting a family and saving for retirement mutually exclusive for all but the top 10% of earners. Add AI job cuts on top of that, and a consumer-led recession seems inevitable.

## The Recession Feedback Loop

Speaking of a consumer-led recession, the enterprise-centric scenario, in which the AI trade seems to have the best bull case, instead turns it into a ticking time bomb. If unemployment substantially decreases consumer spending, then it will reduce revenues and push companies to cut costs further. Eventually, the cutting of costs will find its way back to the top-line revenues of these companies.

Of course, I am not the only one who sees it this way, which is why there has been a resurgence of calls for UBI. Before AI, UBI didn’t make sense because everyone was able to contribute to the economy in a meaningful way. After AI, the job market will be saturated, and the displaced knowledge workers will have nowhere to go and no way to meaningfully contribute to the market. However, it is fair to assume that unemployment will need to reach recessionary levels before policy makers will even get close to passing UBI legislation.

Another bull response is that governments will step in because AI is a strategic necessity. I actually think that is possible. The problem is that it changes the investment thesis. If the bull case increasingly depends on government subsidy, defense contracts, tax incentives, or strategic procurement, then the trade becomes more policy-dependent and less grounded in organic private-sector returns. That may support certain infrastructure winners, but it does not necessarily justify private model-company valuations or the assumption that current AI capex earns attractive economic returns.

The same logic applies to circular financing. I do not think circular financing is the core thesis by itself. The issue is not that it proves fake demand. The issue is that it can pull forward demand, subsidize uneconomic customers, and make revenue quality harder to evaluate. If OpenAI receives infrastructure support in exchange for equity, or if AI vendors recycle investment dollars back into customer contracts, then reported revenue can look cleaner than the underlying economics really are. It also makes costs look cleaner than they are. If compute is being rented at preferred rates, subsidized through strategic deals, or indirectly financed by the same companies booking the revenue, then the current cost structure may not reflect what the business would look like in a normal market.

This is where the fragility comes in. In a simple business, revenue comes from customers, costs come from suppliers, and profit is the difference between the two. In parts of the AI trade, the customer, supplier, investor, and strategic partner can start to look suspiciously like the same circular blob wearing four different Patagonia vests. That makes the whole system much harder to underwrite. Revenue can be overstated because some of it is really capital recycling. Costs can be understated because some of them are being subsidized or deferred through partnerships. Demand can be pulled forward because every company in the chain has an incentive to keep the narrative alive.

Again, none of this means the AI trade is Enron with better GPUs. It just means the margin of safety is lower than the headline revenue growth suggests. If the investment cycle breaks before consumer or enterprise profitability shows up, then revenue quality, cost assumptions, valuations, and capex plans all get questioned at the same time. That is how a normal slowdown turns into an unwind.

That leaves one final bull thesis worth addressing: AGI or ASI.

## The AGI/ASI Bull Thesis

Lastly, I want to touch briefly on the AGI/ASI bull thesis. I have at least 1,500 hours of AI-assisted coding, researching, and general project work at this point, and the intellectual limitations of the LLM transformer architecture are clear to me. I am not going to justify my view here because it gets far too technical and philosophical. This case, at least until a new AI architecture is discovered, is completely impossible in my view and is not worth consideration.

With all of the background laid out, there appear to be only four options worth consideration.

## The Four Possible Outcomes

### 1. Capex cuts and a narrative shift

The first is that investors realize AI spending has gone too far, the narrative shifts, and AI capex takes a nosedive. AI companies will likely all try to continue in an arms race for the strongest model, which will eventually be won by the company with the deepest pockets. In this case, OpenAI and Anthropic will probably cease to exist independently, and Google will most likely come out on top. There will be a sharp correction or crash across the AI trade on the capex cutbacks, plus a surplus of compute resources for multiple years before economically justifiable demand can saturate it.

### 2. Enterprise AI drives mass job cuts

The second is that investors realize enterprise deals are the only route to profitability, and we reach recessionary levels of unemployment within five years. In this case, OpenAI and Anthropic may both continue to exist through multi-year enterprise contracts, and the AI trade will balloon to an incredible size before the worst recession in US history takes hold. A recession that will eventually push policy makers to implement drastic measures like UBI.

### 3. Compute gets cheaper and breaks the capex cycle

The third is that GPU/TPU compute advancements push inference costs to new lows. Bulls would argue that this creates a massive increase in demand and keeps the AI trade going. Maybe. But if demand does not expand faster than efficiency improves, it reduces GPU demand and creates enormous depreciation losses across the industry, while still only maybe providing a route for AI to become profitable without extreme job cuts.

### 4. A new architecture changes everything

The fourth is that a new AI architecture is discovered which cuts inference costs and actually enables eventual AGI/ASI. This would likely be the most important technological discovery in all of human history, even 10 thousand years into the future, and could lead to any number of science-fiction outcomes. The markets would crank, of course.

## Conclusion

In terms of likelihood, the first and second cases seem to hold the most weight to me, as cases three and four require technological discoveries to be made in the next 3-5 years. Of course, reality is not as clear cut as four distinct cases. It will probably be a mix of these, with some added economic turbulence in the meantime.

I am not going to provide trading or position advice, as it is far too dependent on your risk tolerance, portfolio goals, time horizon, etc. I only want to provide my opinion on the considerable risks in the AI bull thesis and why current revenue growth may not last for as long as some people think.

