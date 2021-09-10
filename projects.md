---
layout: page
title: Projects
---

<h1>CURRENT PROJECTS</h1>

<h2>Textual Question Answering System with visual insights</h2>
<p style='text-align: justify;'>Nowadays, We use Natural Language Processing in our everyday life, from  <a href="https://www.amazon.com/b?ie=UTF8&node=21155035011"> sending "virtual" hugs through Alexa </a> to using Google Translate to converse with others when traveling to unfamiliar places. Another application of natural language processing is question answering; a person asks a question, and the machine provides the most accurate response.
<br>
My current project aims to improve textual question answering tasks by providing visual feedback to the machine. The concept is based on how we, as humans, use our intuitions when faced with a problem. For example, if someone asks you, "Who will win a fight, a lion or a deer?" we will use our visual imagination to compare the attributes of the lion and the deer. We can distinguish sharp teeth, big nails, and a muscular body on the lion by visualizing them in our minds and then answering the question. This is something that today's machine question-answering models lack; they understand the language, but they lack visual imagination.
<br>
To close this gap, I'm using the Google search engine to extract visual information for textual question-answering challenges. To improve generated outcomes for textual question answering challenges, a multimodel system that utilizes transformer models (e.g., RoBERTa) and CNN models (e.g., ResNet, VGG) is being developed.
</p>


<!-- <h2>Plot Processing - line plot</h2>
<p style='text-align: justify;'> This project focuses on teaching machines how to understand plots. THe process consists of multiple tasks such as understanding plot type, legends, axis, 
</p> -->


<!-- 
<h2>iViSA: An Adaptive Video Streaming Service over ICN</h2>
<p>Research in Information-Centric Networking (ICN) and Named Data Networking (NDN)
has produced many protocol designs and software prototypes, but they need to be
validated and evaluated by real usage on the Internet, which is also critical to
the realization of the ICN/NDN vision in the long run. This paper reports our
preliminary work on deploying a video streaming service on NDN testbed.

By integrating several building blocks developed by the NDN project and the open-source
community, we implement a system in which users can watch videos through adaptive bit-rate
video streaming service over NDN testbed without installing any software. Initial evaluation
shows satisfactory performance and user experience, but also reveals a number of issues to be
solved. This service is publicly available for Internet users. Visit <a href='https://ivisa.named-data.net'>project's website</a> to watch videos completely over NDN!</p>

<hr>

<h1>OLD PROJECTS</h1>

<h2>NameTrie: An Efficient Data Structure for Name-based Packet Forwarders</h2>
<p>Name lookup is an essential function, but a performance bottleneck in both today and future network
architectures. Variable-length and unbounded names rather than fixed length addresses, as well as much
larger and more dynamic forwarding tables, call for a careful re-engineering of lookup structures for fast,
memory-efficient, and scalable packet forwarding. NameTrie is a project that is mainly focused on designing
a new trie-based data structure to store and index forwarding table entries efficiently and to support fast
name lookups and updates. The novelty of NameTrie lies in the optimal design and implementation of a characte
-trie structure. The nodes of NameTrie are stored compactly, improving cache efficiency and speeding up packet
processing.

Its edges are implemented using a hash table, facilitating fast name lookups and updates. Moreover, in
NameTrie project a new scheme is used to encode some control information without consuming additional
memory, called minASCII. Running on conventional commodity hardware and using large-scale real-world
name datasets, our implementation of NameTrie in software achieves significant speedup for name insertions,
lookups, and removals in comparison to existing schemes, for various datasets with a small memory footprint.
</p>

<h2>MUCA: A New Routing Protocol For Large-scale Caching Networks</h2>
<p>While the Internet has far exceeded expectations, it has also stretched initial assumptions, often creating
tussles that challenge its underlying communication model. Users and applications operate in terms of content,
making it increasingly limiting and difficult to conform to IP’s requirement to communicate by discovering and
specifying a location. To carry the Internet into the future, a conceptually simple yet transformational
architectural shift is required, from today’s focus on where — addresses and hosts — to what — the content
that users and applications care about.The Named Data Networking (NDN) project aims to develop a new Internet 
architecture that can capitalize on strengths — and address weaknesses — of the Internet’s current host-based,
point-to-point communication architecture in order to naturally accommodate emerging patterns of communicatio.
By naming data instead of their locations, NDN transforms data into a first-class entity.

The current Internet secures the data container. NDN secures the contents, a design choice that decouples
trust in data from trust in hosts, enabling several radically scalable communication mechanisms such as
automatic caching to optimize bandwidth. The project studies the technical challenges that must be addressed
to validate NDN as a future Internet architecture: routing scalability, fast forwarding, trust models, network
security, content protection and privacy, and fundamental communication theory. The project uses end-to-end
testbed deployments, simulation, and theoretical analysis to evaluate the proposed architecture, and is
developing specifications and prototype implementations of NDN protocols and applications.</p> 
 -->