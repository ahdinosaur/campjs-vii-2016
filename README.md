# nature's best practices for distributed systems

## hi

i'm [Mikey (@ahdinosaur)](http://dinosaur.is) from [Enspiral](http://enspiral.com)

<div class="row">
  <a href="http://dinosaur.is.com">
    <img alt="Mikey's avatar" src="./avatar.jpeg" width="200" />
  </a>
  <a href="http://enspiral.com">
    <img alt="Enspiral logo" src="./enspiral.png" width="200" />
  </a>
</div>

???

i have no idea what i'm saying

i will use imprecise terminology

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract
- http://www.ribbonfarm.com/2015/03/04/gardens-need-walls-on-boundaries-ritual-and-beauty/
- http://networkcultures.org/unlikeus/resources/articles/what-is-a-federated-network/

## overview

- introduction
- natural networks
- global peer-to-peer networks
- local peer-to-peer networks

## introduction

### systems 101

- networks: who you connect to
- messages: what you say
- signaling: how you connect

examples: 

- ecological systems
- socio-economic systems
- political systems

???

### why nature?

nature is better at distributed systems than we are.

???

life is hard to kill: try killing the fungus spores in your fridge

the planet will survive climate change, will we?

### coordination problems

a coordination problem is where:

- everyone agrees that certain actions would be best
- not everyone is coordinated in taking those actions

example: climate change

???

> Coordination problems are cases in which everyone agrees that a certain action would be best, but the free market cannot coordinate them into taking that action.

- http://www.raikoth.net/libertarian.html#coordination_problems

every intelligent person knows climate change is a problem to be solved.

yet we're not doing enough to solve it.

### stigmergy

central planning and control is a common solution to coordination problems.

yet biological systems make decisions and respond to stimuli:

- without a centralized coordinator
- under severe constraints

???

> Most biological systems are distributed and must make decisions and respond to stimuli without a centralized coordinator and under severe constraints (energy conservation, limited communication range, limited messaging language, among others)

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract
- https://en.wikipedia.org/wiki/Stigmergy

## natural networks

### simple over complex

<img class="center" src="./complex-vs-simple-communication.png" height="500" />

???

rather than sophisticated synchronous protocols (like the OAuth dance),

most natural systems communicate with simple asynchronous messages

### randomized over deterministic

<img class="center" src="./deterministic-vs-randomized-algorithms.png" height="500" />

???

> A stochastic event or system is one that is unpredictable due to the influence of a random variable.

- https://en.wikipedia.org/wiki/Stochastic

### beeping

<img class="center" src="./beeping.png" height="500" />

fly brains specialize cells with Max Independent Set

???

beeping: 

> Beeping: The beeping model17 (Fig- re 2a) assumes the only message hat can be sent or received is a beep (a unary signal). The model assumes an anonymous broadcast network in which nodes have no knowledge about the topology of the network or even an upper bound on its size. In each time slot a node can either beep or be si- lent. At a particular time slot, beeping nodes receive no feedback (they can- not determine if other nodes beeped as well), while silent nodes can only differentiate between two states: none of its neighbors beeping, or at least one neighbor beeping. Such a model is also appropriate for cellular signaling net- works as discussed here.

fly brains: developing fly brains select a subset of cells to become sensory bristles on the fly's forehead.

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract

### stone-age

<img class="center" src="./stone-age.png" height="500" />

???

![](./slime-mold-routing.jpg)

> Foraging slime molds have also been shown to adaptively adjust their networks of tubular junctions based on the distribution and availability of food sources in the area, which is typically unknown a priori. 52
> Slime molds also forage using breadth-first search using real cellular material, which is later pruned when optimal paths are found.  

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract
- http://www.wired.com/2010/01/slime-mold-grows-network-just-like-tokyo-rail-system/

### population

<img class="center" src="./population.png" height="500" />

harvester ants forage for food with Transmission Control Protocol (TCP)

???

> A recent study demonstrated that with limited communication, ants solve the foraging problem by implementing a version of the Transmission Control Protocol (TCP), which is used on the Internet to determine available bandwidth when routing packets. If packet acknowledgments (ACKs) are received quickly, the sender assumes bandwidth is available and boosts transmission; but if ACKs are returned slowly, the sender assumes the network is congested and throttles down transmission. Similarly, the important factor for the ants is the rate of antennal contacts (a binary indicator) between ants currently in the nest and successful ants (with food) returning to the nest. If the rate of contact is high, it implies food in the environment is plentiful, and thus outgoing ants also leave the nest at a faster rate.

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract
- http://priceonomics.com/the-independent-discovery-of-tcpip-by-ants/

### fractals

example:

- human organism
- -> organs
- -> tissues
- -> cells
- -> organelles
- -> large molecules
- -> small molecules
- -> atoms
- -> particles

???

blood-brain barrier protects brain from bad actors.

example: brains are composed of fractal agents

> For our purposes, an agent is an entity capable of autonomous, intelligent, goal-directed behavior.

![](agency-in-the-brain.png)

> Thus there is, in this view, an internal 'economy' in the brain, in which neurons must compete with each other for resources. This design stands in contrast to the standard, Von Neumann computer architecture, whose parts never have to worry about where their energy is coming from. Without resource contention, there's no need for selfishness. And this is, in part, why computers are less flexible and adaptable — less plastic — than brains.

???

- http://www.meltingasphalt.com/neurons-gone-wild/
- https://blog.dinosaur.is/life-as-a-holon/
- Aida, K., Natsume, W. and Futakata, Y. Distributed computing with hierarchical master-worker paradigm for parallel branch and bound algorithm.  In Proceedings of the 31 st International Symposium on Cluster Computing and the Grid.  IEEE Computer Society, Washington, DC, 2003.  

### small worlds

![](./speed-vs-robustness.png)

> A small-world network is a type of mathematical graph in which most nodes are not neighbors of one another, but most nodes can be reached from every other node by a small number of hops or steps

???

> For example, dense topologies with clique-like structures are often used in instances where little-to-no noise is expected, whereas sparser topologies are preferred when networks are expected to face more noise.40
>
> Of course, spars- er topologies are also less efficient (in terms of routing distance, for example) which means execution times will be longer for such topologies. Weakly linked modules, on the other hand, can isolate occasional noise into nearly independent modules that each per- form efficiently.56

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract

> Small-world properties are found in many real-world phenomena, including websites with navigation menus, food chains, electric power grids, metabolite processing networks, networks of brain neurons, voter networks, telephone call graphs, and social influence networks.
>
> Networks of connected proteins have small world properties such as power-law obeying degree distributions.[9] Similarly transcriptional networks, in which the nodes are genes, and they are linked if one gene has an up or down-regulatory genetic influence on the other, have small world network properties.[10]
>
> It is hypothesized by some researchers such as Barabási that the prevalence of small world networks in biological systems may reflect an evolutionary advantage of such an architecture. One possibility is that small-world networks are more robust to perturbations than other network architectures. If this were the case, it would provide an advantage to biological systems that are subject to damage by mutation or viral infection.
>
> By contrast, in a random network, in which all nodes have roughly the same number of connections, deleting a random node is likely to increase the mean-shortest path length slightly but significantly for almost any node deleted. In this sense, random networks are vulnerable to random perturbations, whereas small-world networks are robust. However, small-world networks are vulnerable to targeted attack of hubs, whereas random networks cannot be targeted for catastrophic failure.
>
> Appropriately, viruses have evolved to interfere with the activity of hub proteins such as p53, thereby bringing about the massive changes in cellular behavior which are conducive to viral replication.

https://en.wikipedia.org/wiki/Small-world_network


### handling failure

instead of using sophisticated consensus algorithms, nature uses toplogical features to handle failures.

![](./toplogy-on-speed-and-robustness.png)

???

example: viruses, cells 

> In distributed computing, failures have primarily been handled by majority voting methods, 37 by using dedicated failure detectors, 25 or via cryptography.  41 In contrast, most biological systems rely on various network topological features to handle failures.

...

> underlying network topology. For example, activity-dependent plasticity of synapses is a well-known phenomenon by which neural networks are shaped by environmental stimuli. These sig- nals are processed in a streaming fash- ion, and input patterns can change the topology of the networks designed to
process them.

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract

## global distributed networks

### example: internet service providers

> The very fabric of the Internet can be torn apart by a malicious ISP or even an honest mistake. On April 8th, 2010, an employee at China Telecom misconfigured a router - causing widespread Internet outages lasting up to fifteen minutes.

- [cjdns project goals](https://docs.meshwith.me/project-goals.html)

???


- Pakistani ISP uses BGP to blackhole internet

### example: global registries

CA certs and DNS are based on central registries.

Namecoin distributes the protocol, but not the registry.

???

- how do we deal with multiple nicknames in real life?

### example: mobile network providers

i have phone with a radio, you have phone with a radio, we can't connect because a base station is down.

peer -> middleman -> peer

### example: buying a bicycle with Bitcoin

let's say i'm buying a bicycle from a neighbor.

with Bitcoin, i have to send a message to random strangers (miners) to participate in a global consensus process.

???

- cost of Bitcoin global consensus is large amounts of duplicate CPU work in Proof-of-Work cycles
- within a very few degrees of trust separation from my neighbor, we could be doing local consensus
- cost of Ethereum global computation is large amounts of duplicate memory and CPU work in computation cycles

https://blog.dinosaur.is/global-vs-local-systems/

### example: downloading a file with Bittorrent

when i download a file with Bittorrent, i connect to random strangers.

this means it's easy to monitor who is downloading what.

### example: twitter abuse

since everyone is connected to everyone, there's no barrier to abusing someone on Twitter.

the victim (defender) is the one who has to expend energy rather than offender.

???

open by default

- also easy to spam
  - email
  - distributed hash tables

### example: monoculture

the world is converging on a uniform culture, at the expense of diversity.

- what narratives and metaphors do you use to express your world view?
- how might these bias or blind your thinking?

???

- https://github.com/RichardLitt/endangered-languages

reality is neither objective nor global.

> Westerners, he says, prefer to understand things as mechanisms, while the Chinese prefer to understand things as organisms — and these are two very different kinds of processes.

- http://www.meltingasphalt.com/technical-debt-of-the-west/

reality is subjective and local.

- https://github.com/ssbc/secure-scuttlebutt/issues/86

## local peer-to-peer networks

### why local?

> On the biological side, as technology continues to improve and sheds light on molecular and cellular decision-making, we believe computational perspectives will be essential to understand how local, distributed rules give rise to robust, global systems.

???

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract

- planet ecology

### systems of the future

- networks: you connect to local agents (based on social or geographic proximity)
- messages: you say things subjective to your view
- signaling: you use gossip protocols to relay information

### local agents

- individual
- professional
  - [family](https://github.com/enspiral-root-systems)
  - [community](http://devacademy.co.nz)
  - [network](http://enspiral.com)
- regional
  - subhurb
  - city
  - state

### subjective views

- my friends call me Mikey
- my parents call me Michael
- i call myself dinosaur

### gossip protocols

relay a message through who's local to you.

example: i run into Alice in town. "hey what's the lastest you've heard from Bob?"

???

> [biological] message sizes are usually one bit or of constant size indicting that unlike many traditional distributed algorithms, biological processes do not use such an identifier to label the sender and receiver

blockchain message gossip

- https://en.wikipedia.org/wiki/Gossip_protocol
- https://github.com/ssbc/scuttlebot
- https://github.com/substack/swarmbot

### example: secure scuttlebutt (SSB)

peer-to-peer log store:
 
- each user has a feed associated with a public and private keypair
- each feed is a linked list of message signed with the associated private key
- messages can reference each other to create links (and indexes)
- each user gossips with who they "follow", and who those users "follow"
- public messages are plain JSON objects
- private messages with the public key of the intended recipient
  - try to decrypt to see if it is for you

### example: Patchwork

peer-to-peer social network:

- each user can create "about" messages for any other user (name, avatar, ...)
- any user can create "post" messages which provide Twitter / Facebook style communication

### example: [git-ssb](https://github.com/clehner/git-ssb)

decentralized GitHub!

### demos

## thanks

:3

- [Patchwork](https://ssbc.github.io/patchwork): proof-of-concept for truly distributed social network
- [scuttlebot](https://scuttlebot.io): underlying peer-to-peer log store
- [Value Flows](https://valueflo.ws): protocols for fractal socio-economic systems
