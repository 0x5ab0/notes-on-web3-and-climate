**Source:** ["Unpacking Ton-Year Accounting" by CarbonPlan](https://carbonplan.org/research/ton-year-explainer)

# Introduction

To reach net-zero and limit global warming, we need to cut emissions and **permanently remove CO₂** from the atmosphere. However, significant investment is going into shorter-term interventions that either delay emissions or remove carbon for temporary storage, usually involving forestry and agricultural activities.

There is **no clear framework to assess the climate benefits of temporary carbon storage**; answers vary based on which climate outcomes are considered and depend on normative decisions (e.g., the time horizon over which value is calculated).

Despite this, many equate the benefits of temporary carbon storage with the impacts from carbon emissions, either implicitly (i.e., an offset credit representing 10, 50, or 100 years of carbon storage used to justify the emission of a ton of CO₂) or explicitly (i.e., ton-year accounting methods, which value carbon storage based on its duration, used by companies to bundle short-duration carbon storage, such as 1-year forest harvest delays).

Different **ton-year accounting methods** paint different pictures about the value of temporary carbon storage. This article helps describe:
- How ton-year accounting works.
- Its implicit assumptions about the valuation of temporary carbon storage.
- The differences between the most prominent ton-year accounting methods.

It also develops two **analytical conclusions**:
1. Explains that the **Moura Costa method** produces physically invalid results and should not be used to credit temporary carbon storage.
2. Reviews the optional use of **discount rates**, which break any claims to "physical equivalence" that might otherwise be made using ton-year accounting methods.

# Basics

**Ton-year accounting** is a family of techniques for calculating how many tons of temporarily stored CO₂ are physically equivalent to avoiding the emission of CO₂ in the first place. A central idea in ton-year accounting is that the climate impacts of CO₂ can be characterized by the quantity of CO₂ involved and the time it resides in the atmosphere, so a larger quantity of CO₂ stored for a shorter period of time and a smaller quantity of CO₂ stored for a longer period of time can claim equivalent climate outcomes.

### Step 1. Defining a new unit

**Goal:** Define a unit that captures both the number of tons stored and the time over which those tons are stored.

A **ton-year** is defined simply as **1 tCO₂ held somewhere for one year**. A tree that holds 1 tCO₂ for 2 years provides 2 ton-years of carbon storage, and a tree that holds 2 tCO₂ for 10 years provides 20 ton-years.

### Step 2. Dealing with time

**Goal:** Decide how to value costs and benefits that occur in the future.

The **time horizon** is the point past which the costs and benefits of carbon storage are ignored. The shorter the time horizon, the more valuable temporary carbon storage will seem. Choosing a time horizon is a _normative_ judgement rather than the expression of a scientific consensus or physical reality.

### Step 3. Calculating the ton-year cost of an emission

**Goal:** Calculate the cost of an emission in ton-years.

If CO₂ stayed in the atmosphere permanently, the ton-year impact of an emission would be the quantity of CO₂ multiplied by the time horizon chosen in Step 2. In reality, we also need to account for the parts of the global carbon cycle that remove CO₂ from the atmosphere naturally.

In the following example, 1 tCO₂ is emitted at t=0 and removed from the atmosphere by natural processes over four years. The emission’s ton-year impact is summed over the time horizon to calculate the total ton-year cost of the emission. This example is physically unrealistic because real CO₂ emissions affect atmospheric CO₂ concentrations for millennia.

![Example of ton-year emission cost calculation](https://user-images.githubusercontent.com/81234139/169811866-b1ec1752-13eb-4377-b6ee-253364ef3591.png)

### Step 4. Calculating the ton-years of a carbon storage solution

**Goal:** Calculate the benefit of a temporary carbon storage project in ton-years.

There are many methods for this benefit calculation, the most prominent ones being the **Moura Costa** and **Lashof** methods.

- **Moura Costa** consists in counting up the number of tons stored and multiplying by the storage duration, thus _not_ directly quantifying atmospheric outcomes nor considering the potential impact of re-emission after the temporary storage period.
- **Lashof** looks only at atmospheric outcomes and assumes that temporarily stored carbon is fully re-emitted at the end of the storage period. It calculates the benefit by asking how many ton-years of atmospheric impact are _avoided_ within the specified time horizon, so if temporary carbon storage pushes some of the impact of an emission out past the chosen time horizon, Lashof considers that a quantifiable benefit.

In the following example, a project stores 1 tCO₂ in a tree for two years, then re-emits that carbon into the atmosphere. The emitted CO₂ is removed from the atmosphere by natural processes over four years. Moura Costa calculates a 2 ton-year benefit, while Lashof calculates a 0.5 ton-year benefit. This example is physically unrealistic because real CO₂ emissions affect the atmosphere for hundreds of thousands of years.

![Example of ton-year emission benefit calculation using the Moura Costa and Lashof methods](https://user-images.githubusercontent.com/81234139/169814519-8aee9b81-ac1a-422a-95a2-76266115c397.png)

### Step 5. Making an equivalence claim

**Goal:** Determine how much temporary storage is needed to offset an emission.

Both methods answer this question by **dividing the ton-year cost of emissions by the ton-year benefit of temporary storage**, which produces a unitless equivalence ratio.

To complete our example scenario:
- Under **Moura Costa** accounting, storing 1 tCO₂ for two years is enough to offset 100% of the CO₂ emission (2 ton-years / 2 ton-years = **equivalence ratio of 1**).
- Applying **Lashof** to the same project says that we would only offset 25% of the emission, meaning we would need to scale the project four-fold to claim equivalence (2 ton-years / 0.5 ton-years = **equivalence ratio of 4**).

Despite these divergent outcomes, either method might be used to bundle temporary carbon storage into a carbon offset and problematically, both of these offsets could be marketed as equivalent to 1 tCO₂.

# Climate Outcomes

We need to ask how ton-year equivalence claims relate to the climate outcomes we care about.

To start, we must consider a more **realistic representation** of **how carbon emissions affect atmospheric CO₂ concentrations**. Rather than explicitly incorporating the natural processes within the Earth’s biosphere and oceans, which operate over large timescales, ton-year accounting methods instead rely on simplified, modeled "**impulse response function** curves that characterize the proportion of a CO₂ emission remaining in the atmosphere as a function of time.

![Ton-year methods calculate the ton-year cost of CO₂ in the atmosphere by integrating under a curve that represents the proportion of an emission remaining in the atmosphere as a function of time](https://user-images.githubusercontent.com/81234139/169826996-40e587b5-9f30-46f2-9efe-bdad2625c1f9.png)

### Cumulative Radiative Forcing

When ton-year accounting takes the integral of the CO₂ emission curve, it approximates the amount of extra energy trapped in the climate system by a CO₂ emission — a concept known as **cumulative radiative forcing**. Excess energy trapped in the climate system causes harmful and effectively irreversible climate impacts, like glacier melt and sea-level rise, so even temporary reductions yield positive climate benefits.

Emitting CO₂ results in a quantifiable amount of extra energy being added to the climate system. We can also calculate how much less energy is added to the climate system because of temporary CO₂ storage. When these two quantities balance out, ton-year accounting can claim that the emission and the temporary storage are **equivalent from the standpoint of cumulative radiative forcing**.

We have to ask if this version of _equivalence_ is sufficient even though it ultimately involves a critical normative judgment: the timeframe over which the ton-year comparison is made. Moreover, cumulative radiative forcing is not the only climate outcome we care about: there are other climate impacts which are primarily determined by the absolute amount of CO₂ in the atmosphere at a given point in time, rather than the total energy trapped in the climate system over time, and in these cases, storing a ton of CO₂ today but releasing it decades from now may simply postpone the problem.

It’s absolutely possible that temporary carbon storage looks beneficial through the lens of cumulative radiative forcing, but may be neutral or even counterproductive through the lens of temperature targets after the temporary storage ends. Unfortunately, there is no objective framework for balancing these potentially contradictory outcomes.

Ton-year accounting **does not attempt to resolve this tension** — it simply operates with an **implicit assumption that cumulative radiative forcing is the climate outcome we should pay attention to**. For some climate impacts and time horizons, that’s probably a reasonable approximation. For others, the assumption doesn’t hold.

### A Critique on the Moura Costa Method

**Different ton-year methods produce different claims** about the benefit of the same temporary carbon storage. For a project that stores 1 CO₂ for 20 years before re-emitting it to the atmosphere and a 100 year time horizon, Moura Costa calculates a 20 ton-year benefit while Lashof calculates an 8.4 ton-year benefit.

<div>
  <img src="https://user-images.githubusercontent.com/81234139/169834342-aa1a41a0-fe1b-49ae-ac07-b02e085086f0.png" />
  <img src="https://user-images.githubusercontent.com/81234139/169834401-b616a50c-3886-4c08-aa64-a9214840318d.png" />
</div>

If Moura Costa and Lashof are both making physical equivalence claims about the same temporary storage, how can they come up with different answers?

For **Lashof**, we can compare atmospheric outcomes for the emission scenario and the project scenario (with the temporary CO₂ storage scaled according to the equivalence ratio) to confirm that the physical claim is consistent from the standpoint of cumulative radiative forcing. Everything checks out.

When we try to do this for **Moura Costa**, however, we encounter a problem. To compare atmospheric outcomes, we have to look at what happens to the CO₂ between the end of the temporary storage period and the end of the time horizon. Since Moura Costa’s calculations don’t pay any attention to what happens after the temporary storage period, many different atmospheric outcomes (e.g., full re-emission, partial re-emission, or transition to permanent storage) can all be assigned the same nominal benefit, despite having obviously different physical consequences. Furthermore, if we assume full re-emission (as above), the physical equivalence claim doesn’t hold up.

It is also true that by comparing the ton-years of CO₂ in the atmosphere directly to the ton-years of CO₂ in storage, Moura Costa distorts the core, physical logic of ton-year accounting and significantly exaggerates the climate benefits of temporary storage. A clear illustration of this problem is that **Moura Costa allows for the claim that temporarily storing 1 tCO₂ justifies the emission of more than 1 tCO₂**, an indefensible outcome:

<table>
  <tr>
    <th>Storage amount</th>
    <th>Storage period</th>
    <th>Equivalent emissions</th>
  </tr>
  <tr>
    <td>1 tCO₂</td>
    <td>25 years</td>
    <td>0.48 tCO₂</td>
  </tr>
  <tr>
    <td>1 tCO₂</td>
    <td>50 years</td>
    <td>0.95 tCO₂</td>
  </tr>
  <tr>
    <td>1 tCO₂</td>
    <td>75 years</td>
    <td>1.43 tCO₂</td>
  </tr>
    <tr>
    <td>1 tCO₂</td>
    <td>100 years</td>
    <td>1.91 tCO₂</td>
  </tr>
</table>

With a time horizon of 1000 years, the cost of an emission is about 310 ton-years. Lashof calculates that 1 tCO₂ stored for 1 year would result in an approximately 0.235 ton-year benefit, so for “equivalence”, we’d need to store about 1319 tCO₂ for 1 year (310.161 / 0.235 = 1319.45). Moura Costa, in contrast, calculates we need to store only around 310 tCO₂ for 1 year (310.161 / 1 = 310.161). Changing the time horizon to 100 years drops the Lashof and Moura Costa equivalence claims to 128 tCO₂ and 52 tCO₂ stored for 1 year, respectively.

### Discount Rates

NCX’s current white paper asserts that temporarily storing 30.8 tCO₂ for one year is equivalent to the impact of emitting 1 tCO₂. While we understand that NCX markets its approach as using a distinct methodology, our analysis shows that their approach is conceptually identical to the Lashof method with one important difference — NCX’s ton-year calculations apply a **3.3% discount rate**.

The choice to apply a discount rate is more complicated than it may appear.

If the goal of ton-year accounting is to **produce equivalence claims about physical climate outcomes**, applying a discount rate breaks that relationship and invalidates any claim to physical equivalence. Both temporary carbon storage and emitting CO₂ result in quantifiable changes to the Earth’s energy balance and we should compare them directly, no discounting required.

If instead the goal is to **produce equivalence claims about economic outcomes**, things get more complicated. Calculating the economic value of temporary carbon storage requires translating CO₂ emissions into economic damages. To do this, economists use “damage functions” that take variables like future temperatures and sea-level rise as inputs and generate costs in terms of dollars. Climate economists apply discount rates to those calculated costs to represent them in net present value calculations. There are good reasons to think about the economic trade-offs of different climate solutions via net present value calculations, but doing so adds layers of complexity and normative decision-making that must be navigated with care.

By applying a discount rate, NCX makes an economic equivalence claim rather than a physical equivalence claim. The specifics of their approach to economic valuation raise significant questions about their claimed equivalence ratios, which we’ve written about in an accompanying blog post. We are also concerned that NCX markets its credits as producing “equivalent climate impacts” compared to permanent carbon storage, when in fact the use of a discount rate allows for greater climate impacts tomorrow in exchange for temporary climate benefits today.

# Key Takeaways

**1.** The diversity of ton-year methods allows different quantities of temporary carbon storage to be marketed as equivalent to 1 tCO₂, which is why it’s **important to surface what assumptions** — like the choice of a time horizon or application of a discount rate — **underlie all ton-year claims**.

**2.** Ton-year accounting is **only useful for making equivalence claims about climate damages that stem from cumulative radiative forcing**. It’s true that temporarily storing carbon reduces the cumulative amount of energy trapped by the Earth’s atmosphere, but that does not make it identical to either avoiding emissions in the first place or permanently storing CO₂ — both of which produce benefits that are strictly greater than those achieved by temporary carbon storage.

**3.** The **claims made by the Moura Costa method are not physically credible** and the method should not be used to establish climate-equivalence claims or issue carbon offsets. Moreover, the **application of discount rates within ton-year accounting invalidates claims of physical climate equivalence** and can obscure the atmospheric consequences of temporary carbon storage.

Moving forward, it is critical to develop a clear and consistent framework for articulating the value of temporary storage. We’re especially excited to see new efforts to integrate the value of temporary storage into conversations about the social cost of carbon, an approach that explicitly links the value of temporary-ness to robust conversations about quantifying and discounting future climate harms.

Temporary storage has a non-zero value, but it’s important to be open and transparent about both the risks and benefits that come when valuing temporary storage — both of which may vary depending on the relative value society places on different kinds of climate impacts. More work is needed to establish a coherent framework for valuing temporary storage.
