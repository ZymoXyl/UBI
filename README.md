# UBI
A framework for simulating dynamic effects of UBI (work in progress!)

This is a very ambitious project to simulate the effects of introducing a UBI policy on a number of target economic parameters of interest. This reserach is tailored to the US but the hope is that the model is general enough to function in any market ecoomy. We consider dynamic effects induced by the interactions of a population of individuals, firms, and the government. Here's a brief summary of how we're treating each of the agents udner consideration (a lot of this is still TBD):

* Populations of individuals - Rather than explicitly instantiating 100 million + individuals, we are instead considering a population (of a given size) with a joint distribution of income and wealth. Individuals are modeled as having (for now) homogeneous preferences regarding consumption and labor. Individuals are taxed according to their income and receive rebates according to their eligibility for welfare programs. For now we will keep the population constant across time, and not consider any migration effects induced by UBI.
* Government - The government collects taxes on individuals' and corporations' net income via progressive tax policies. The government also has expenditures via welfare programs - which provide benefits to individuals - and other net expenditures (a constant for now). Note that we are not considering monetary policy.
* Firms - Behavior TBD

A welfare program is defined as a program which provides a benefit to an individual X with income Y given by:
B(X,Y)=E(X)∗min{G + S * Y, M, max[M−T(Y −P),0]}
Where:
* E(X) is an indicator variable reflecting an individual's eligibility for the welfare program
* G is the grant for an individual with 0 income
* S is the subsidy on income (e.g. the earned income tax credit policy has positive S)
* M is the maximum benefit
* P is the income level above which benefits begin to phase out
* T is the tax on additional income above P

A welfare program also has associated with it an efficiency coefficient which indicates what percentage of resources allocated to it go to welfare (as opposed to overhead costs), and a coefficient reflecting participation rates of the program (which are affected by factors such as social stigma surrounding the program).

A UBI policy is a special case of a welfare program in which G = M is very large, and P is either very large or nonexistent. A UBI also has 100% participation and very high efficiency.


In this model, we will consider and attempt to quantify the following effects:

1. First-order effects on the cost of such a program, and what changes could be made to the tax policy to address this
2. Based on the UBI and the new tax policy, higher-order effects on labor supply (substitution and wealth effects), consumer demand, inflation, economic productivity, wealth distribution, poverty, GDP, educational attainment, etc.
3. Short-term and long-term market equilibria resulting from UBI.

The hope is that this research will have practical implications and will serve to enhance understanding and discussion of the UBI policy and the federal welfare system in general. The model described here will leave a lot of parameters open to be filled in with results from empirical economic research. For now, I am mainly concerned with formalizing the model itself and detailing its implicit assumptions and limitations.


This is a very ambitious project in its primitive stages, and if you're reading this and want to help out, I would absolutely love to hear from you. You can email me at b.r.lampert@gmail.com.
