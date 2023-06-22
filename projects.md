---
layout: page
title: Projects
---

# Projects

## OD-TQA: On-Demand Visual Grounding for Textual Question Answering

<p style='text-align: justify;'>
    We often underestimate the power of visualization. The human brain is incredibly adept at interpreting and extracting information from visual stimuli, allowing us to form complex conclusions based on what we see. This integral human capability is often taken for granted, especially when it comes to the field of Natural Language Processing (NLP).
    <br>
    NLP has transformed our digital interactions, from instant translations that bridge language gaps, to AI models like <a href="https://medium.com/predict/i-prompted-chatgpt-to-write-futurist-science-fiction-stories-the-results-are-underwhelming-49adcb9bf473"> ChatGPT that can generate enthralling Sci-Fi narratives in a writer's specific style.</a> In the realm of question answering, AI is typically tasked with finding the most accurate response to a query. However, most models lack a crucial dimension that humans use in decision-making: visualization.
    <br>
    In my current project, OD-TQA, I'm addressing this gap by augmenting textual question answering systems with visual grounding capabilities. Using Google search, I extract relevant images that provide crucial visual information corresponding to the question at hand.
    <br>
    The OD-TQA project brings together the power of Transformers like RoBERTa and Convolutional Neural Networks (CNNs) like ResNet and VGG, creating a multimodal system. This innovative fusion not only enhances the AI's interpretative power but also provides richer, more context-aware responses.
    <br>
    OD-TQA's structure, seen below, serves as an excellent example of an innovative solution that captures the multimodal nature of human cognition. It strives to replicate the way we, as humans, synergize multiple forms of information—textual, visual, and more—to understand and interact with the world around us.
</p>

![OD-TQA structure](/assets/papers/VTQA_dataset_4.png) 

<p style='text-align: justify;'>
    As OD-TQA continues to evolve, the project's ultimate goal is to bridge the gap between human and machine cognition, creating AI systems that can understand and interpret the world just as richly as we do. This endeavor encapsulates my broader research interests in Deep Learning and Multimodal Machine Learning. It promises a future where AI is not just a tool for answering questions, but a partner in exploring the complexities of our world.
</p>




## DeepShallow Network: An Innovative Architecture for Time-Series Forecasting

<p style='text-align: justify;'>
    In a world driven by data, effective analysis and prediction of time-series data is crucial. From predicting stock market trends to forecasting city traffic, the applications of time-series forecasting are far-reaching and vital. However, traditional methods often stumble when addressing the inherent variability of temporal data's significance, leading to inefficient and less accurate predictions.
    <br>
    My DeepShallow Network project proposes an innovative solution to this issue. It is a novel Convolutional Neural Network (CNN) architecture specifically designed for time-series forecasting tasks. The unique aspect of the DeepShallow network lies in its flexibility—it adjusts the depth of the network layers based on their temporal distance from the prediction point. This results in a more profound analysis of historical data while providing a shallower, more direct interpretation of recent data.
</p>

![DeepShallow Architecture](/assets/papers/DeepShallowFigure.png)

<p style='text-align: justify;'>
    Crucially, the DeepShallow network introduces a weight-sharing mechanism across the same depth of convolutional layers at different timestamps. This innovative feature fosters better generalization, reducing the model's susceptibility to overfitting. It's a direct response to the limitations of fixed-depth architectures, offering improved accuracy in various forecasting tasks.
    <br>
    I have demonstrated the DeepShallow Network's practical effectiveness in two diverse use-cases: rush-hour traffic prediction in Manhattan, using NYC Taxi TLC Trip Record Data, and flight-level passenger traffic prediction using historical traffic, price closure data, and seasonality. These case studies not only exemplify the network's wide-ranging applicability but also underscore its potential in handling diverse time-series forecasting tasks.
    <br>
    The DeepShallow network offers a fresh perspective in the field of time-series forecasting. It leverages the power of deep learning while recognizing and responding to the nuances of temporal data, underscoring my commitment to developing more intelligent, adaptable AI solutions.
</p>




<!-- 
<h1>CURRENT PROJECTS</h1>

<h2>OD-TQA: On Demand Visual Grounding fot Textual Question Answering</h2>
<p style='text-align: justify;'>

    In today's world, we use Natural Language Processing (NLP) in various aspects of our lives, from using Google Translate to communicate with others in unfamiliar places, to using <a href="https://medium.com/predict/i-prompted-chatgpt-to-write-futurist-science-fiction-stories-the-results-are-underwhelming-49adcb9bf473"> ChatGPT to generate Sci-Fi stories in the style of our favorite writers </a>. Another common application of NLP is question answering - a person asks a question, and the machine provides the most accurate response.
    <br>
    My current project aims to enhance the capabilities of textual question answering systems by incorporating visual feedback. As humans, when faced with a problem, we often use our intuitions and visual imagination to guide our decision making. For example, if someone asks, "Who would win in a fight, a lion or a deer?" we can visualize the attributes of each animal, such as the lion's sharp teeth and strong muscles, and use that information to make an informed decision. However, current machine question answering models do not have this ability to visualize and use that information to generate responses.
    <br>
    To bridge this gap, I am using Google search to extract visual information for textual question answering tasks. To further improve the performance of these models, I am also developing a multimodel system that combines transformer models (such as RoBERTa) with CNN models (such as ResNet and VGG). This system has the potential to provide more accurate and informed responses to question answering tasks by leveraging the strengths of both types of models.
</p>

![OD-TQA structure](/assets/papers/VTQA_dataset_4.png) -->





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

