# Blackbird Project
Blackbird is a neuromorphic system-on-chip (NeuroSoC) aimed at reconfigurable computing and hardware acceleration.
## Why the human brain
The human brain, the most complex structure in the known universe, has a power consumption of just 20W [Attwell et al., 2001](https://pubmed.ncbi.nlm.nih.gov/11598490/)). It can process, analyze, and even generate novel ideas using the power equivalent to of a LED light bulb. This remarkable efficiency is the primary inspiration for neuromorphic computing, it takes inspiration of the brain, how it works, communicates and tries to replicate its behaviour (side note, 80% of the 20W power is used with  neural signaling and the postsynaptic effects [Attwell et al., 2001](https://pubmed.ncbi.nlm.nih.gov/11598490/)).
## What are the parts of the Blackbird NeuroSoC
The Blackbird needs two fundamental parts (it needs more than two parts in between, but this is a gross oversimplification), because not everything can be digital or analog, it needs both worlds in different ratios to work as the human brain [Sarpeshkar et al., 1998](https://pubmed.ncbi.nlm.nih.gov/9744889/).
### Analog core, everything is analog and fast

The Neurosoc has a central processing node, lets call it an analog accelerator, said accelerator will have these parts (work in progress):

- Reconfigurable matrix
- Zig-Zag power scheme or low power state
- Low voltage spiking neurons
- Reconfigurable synapses
- Memory module for configuration storage
- Synaptic weights (floating gate or memristors) 
- Adjustable neuron parameters
- Data converters (DAC and ADC)

### Digital core, we communicate in digital 
Analog is great and all, but well we don't use analog communication anymore (landlines are going extinct D:).
Digital core is responsible for everything regarding:
- Communication in and out
- configuration of the io, behaviour of neurons and so on
- transfering the information to the SoC
- Communication with external sources (internet, sensors, etc)
- debug and analysis of data

## Repository structure

```
project-root/
├── designs/              # Your design files (mounted in container as /foss/designs)
│   ├── libs/            # Design libraries
│   ├── simulations/     # Simulation results
│   └── setup_pdk.sh     # PDK setup script
├── start_vnc.sh         # Container launch script (Unix/Linux/Mac)
└── README.md            # This file
```
