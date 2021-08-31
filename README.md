# Single-Cycle Climate Solutions

## Project Goal
**Identify the largest reduction in greenhouse gas emissions that a region can accomplish in a single election cycle using region-specific tactics.** SCCS does this using dynamic simulation modeling with data and tactics provided by modelers and citizen scientists.

## Key Assumptions

SCCS was created on the following assumptions:

1. Climate solutions can be private or public.
1. Private individuals and companies have made as much change to address climate change as they are able to make given their circumstances. Further private change is either blocked by infrastructure (e.g. can't buy an electric vehicle because there's no EV stations), cost (e.g. can't upgrade my home insulation as other repairs need to happen first, or high taxes on electric vehicles), or cultural barriers (e.g. can't switch to low-meat diet as I'm a rancher and meat is crucial to my identity). 
1. Public climate solutions such as upgrading power grids to use renewable sources -- as well as the removal of blockers to private climate solutions -- are in the hands of policymakers: they are therefore at the mercy of election and/or planning cycles.
1. Policies that fail to be implemented within a single election or planning cycle will fail. Climate solutions, by extension, must therefore be implemented in a single cycle.
1. There are no public, shared 

The role of SCCS is therefore to help regions and the public identify the most effective climate solutions per jurisdiction that can be accomplished in one election or planning cycle. SCCS is decomposed into many pieces, allowing each region to plug and play the solutions relevant to their needs.

The structure of the project is as follows:

```
sccs
	core
		interfaces
		utility classes
		common tactics
			fossil fuel power source
	regions
		region-1
			model
			region-specific opportunities & tactics
		region-2
			model
			region-specific opportunities & tactics
		region-n
			model
			region-specific opportunities & tactics
```

Each Region is a simulation model that reports cost and greenhouse gas emissions. Region have on or more Opportunities, which have Tactics to reduce their greenhouse gas emissions (or bring the opportunity online, e.g. wind farm):

```
Region --has--> Opportunities --modified by--> Tactics
e.g.
Saskatchewan --has--> Coal Plants --modified by--> Carbon Capture & Storage
```


This may include general Tactics such as carbon capture on existing coal plants as well as region-specific Tactics such as installing EV chargers in all rural towns. The Region is then attached to an Experiment, which allows different strategies (i.e. a combination of Tactics) to be evaluated. Experiments exist for exploring single Strategies visually (useful for the general public), for exploring all combinations of Tactics (e.g. to discover the strategies with highest ROI), or for exploring strategies on a budget (i.e. what's the greatest impact that could be made with $1B?).

SCCS is being first applied to Saskatchewan, Canada as the region is sparse, has a heavy reliance on fossil fuels for transport and power generation, and has ongoing incentives to maintain fossil fuel production.

## FAQ

### The Data

#### Where do you get data from?

#### How do you know the data is correct?

### Simulation Modeling

#### What is it and how does it work?

### Contributing

#### Who can contribute?

### I can code: how do I contribute?

#### I can't code: how should I suggest improvements?



