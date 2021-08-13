# Single-Cycle Climate Solutions

The goal of SCCS is simple: identify the largest possible reduction in greenhouse gas emissions that an area can accomplish in a single election cycle. This reduction can come through multiple strategies in multiple sectors.

The assumptions of SCCS are also simple:

1. Consumers have made as much individual change as they are able to make. Further individual change is either blocked by environment (e.g. can't buy an electric vehicle as there's no EV stations), cost (e.g. can't upgrade my home insulation as other repairs need to happen first), or cultural barriers (e.g. can't switch to low-meat diet as I'm a rancher and meat is crucial to my identity).
1. Climate solutions must therefore remove blockers from individuals if individual-level changes are to occur.
1. Climate solutions that are effectively non-individual, such as power grid energy sources, must be actively changed by policymakers.
1. Climate solutions that fail to be implemented within a single election cycle will fail.

The role of SCCS is therefore to evaluate and identify the most effective climate solutions per jurisdiction that can be accomplished in one election cycle. SCCS is decomposed into many pieces, allowing each region to plug and play the solutions relevant to their needs.

The structure of the project is as follows:

```
sccs
	core
		runner
		interfaces
	tactic
		tactic-1
		tactic-2
		tactic-n
	regions
		region-1
			model powered by runner and tactics
			region-specific tactics
		region-2
			model powered by runner and tactics
			region-specific tactics
		region-n
			model powered by runner and tactics
			region-specific tactics
```

Each Region implements a Model that reports cost and greenhouse gas emissions. The Region then includes a set of Tactics to reducing its greenhouse gas emissions. This may include general Tactics such as carbon capture on existing coal plants as well as region-specific Tactics such as installing EV chargers in all rural towns. The Model is then attached to a Runner, which allows different Strategies (i.e. a combination of Tactics) to be evaluated. Runners exist for exploring single Strategies visually (useful for the general public), for exploring all combinations of Tactics (e.g. to discover the Strategies with highest ROI), or for exploring Strategies on a budget (i.e. what's the greatest impact that could be made with $1B?).

SCCS is being first applied to Saskatchewan, Canada as the region is sparse, has a heavy reliance on fossil fuels for transport and power generation, and has ongoing incentives to maintain fossil fuel production.