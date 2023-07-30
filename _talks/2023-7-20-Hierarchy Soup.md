---
title: "Hierarchy Soup"
collection: projects
type: "Federated learning"
permalink: /projects/Hierarchy-Soup
venue: "Summer Intern"
date: 2023-7-20
location: "UT Austin"
---

1. **Problem**:

   Considering a federated learning setting (or CoID Fusion setting), we cannot directly train multiple heterogeneous data domains.

   e.g., If we use the RWS setting (19 corruption types) and standard FL approach, we can observe: 19-heterogeneous-client-FL performance < single-client performance, which means incorporating more **diverse** data will hurt performance.

2. **Our Aim:** Incorporating more data will always lead to better performance

   a. For task A, by adding task B that is similar to task A, the performance of task A will increase

   b. For task A, by adding task C that is dissimilar to task A, the performance of task A will be unchanged or slightly increase.

3. **Assumption(Probably too strong, not sure):**We can decompose model weights based on their specialties, too. 

   Consider three tasks, task A&B can help each other, but C cannot help A&B nor be helped, we hope to find a way to decompose weights so that:

   a. There exist a shared component of weights that encode common knowledge of  task A, B, C, we denote the weight as $$W_{A, B, C}^{0}$$.

   b. There exist a shared component of weights that encode common knowledge of  task A, B, we denote the weight as $$W_{A, B}^{1}$$. Note that $$W_{A, B}^{1}$$ does not contain the knowledge encoded in $$W_{A, B, C}^{0}$$.

   c. $$M_{A}=W_{A, B, C}^{0}+W_{A, B}^{1}+W_{A}^2$$. So task C can update and help the first item, while task B can update and help the first and second item. (I will refer to each item as "Node", since it can be view as a Node on a Tree structure.)

4. **Question: **how to decompose the weights

5. **Method (temp): **By Pareto

   Initialize: $$W_{A, B, C}^{0}=Pretrain-Model, Other-Nodes=0$$

   For cr in 0~total communication round number

6. **Expected Result:**

   group of tasks 1: $$Task_{1\ to\ n}$$, group of tasks 2: $$Task_{1\ to \ n+1}$$

   If we use traditional FL, after the introduction of the n+1 task, performance on some tasks will drop.

   If we use this method, after the introduction of the n+1 task, no performance will drop.

7. **Potential Problem:**

   a. The child node relies on the parent node(step5), which contradicts the	assumption. (Hope Pareto can somehow disentangle the dependency, any other option?).

   b. (same issue as MTLFL) Different clients have different starting points.



