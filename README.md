# Blackbird Project

<img align="left" width="33%" src="/misc/blackbird.png">

Blackbird is a neuromorphic system-on-chip (NeuroSoC) aimed at reconfigurable computing and hardware acceleration. The  core elements for the blackbird platform are interchangeable, modular and has the following elements.

- multiple spiking neuron architectures.
- synapse mechanisms
- control units for memory arrays
- reconfigurable matrix unit


## Why the human brain
The human brain, the most complex structure in the known universe, has a power consumption of just 20W [Attwell et al., 2001](https://pubmed.ncbi.nlm.nih.gov/11598490/)). It can process, analyze, and even generate novel ideas using the power equivalent of an LED light bulb. This remarkable efficiency is the primary inspiration for neuromorphic computing; it takes inspiration from the brain, how it works, communicates, and tries to replicate its behaviour (side note, 80% of the 20W power is used with  neural signaling and the postsynaptic effects [Attwell et al., 2001](https://pubmed.ncbi.nlm.nih.gov/11598490/)).
## What are the parts of the Blackbird NeuroSoC
Any system-on-chip requires two fundamental parts (it needs more than two parts in between, but this is a gross oversimplification), because not everything can be digital or analog; it needs both worlds in different ratios to work as the human brain [Sarpeshkar et al., 1998](https://pubmed.ncbi.nlm.nih.gov/9744889/).
The BlackBird Project aims to create submodules for each peripheral of the SoC and have them available to create larger units with complex designs or keep it simple 
### Analog core, everything is analog and fast

The Neurosoc has a central processing node, let's call it an analog accelerator. This accelerator will have these parts (work in progress):

- Reconfigurable matrix
- Zig-Zag power scheme or low power state
- Low-voltage spiking neurons
- Reconfigurable synapses
- Memory module for configuration storage
- Synaptic weights (floating gate or memristors) 
- Adjustable neuron parameters
- Data converters (DAC and ADC)

### Digital core, we communicate with the world
Analog is great and all, but well, we don't use analog communication anymore (landlines are going extinct D:).
The digital core is responsible for everything regarding:
- Communication in and out
- configuration of the io, behaviour of neurons, and so on
- transferring the information to the SoC
- Communication with external sources (internet, sensors, etc)
- debug and analysis of data

## Repository structure
```
project-root/
├── analog_core/            # Analog core designs
├── digital_core/           # Digital core designs
├── tb_analog_core/         # Analog core designs testbench
├── tb_digital_core/        # Digital core designs testbench
├── documentation/          # Documentation for additional elements and explanations
└── misc                    # miscelanious elements for support or pointing to other repos

