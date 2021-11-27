---
layout: post
title: Landscaping Clinical Natural Language Processing in the United Kingdom 
date: 2021-10-26
author: 
    name: Honghan Wu
categories: article
---
This article aims to present an overall, timestamped and multifaceted understanding of the development of clinical Natural Language Processing (NLP) in the UK.
<!--more-->
Specifically, the main objectives are to gain understanding in the following key aspects:
- Stakeholders: NHS, clinical professionals, informatics researchers, funders, industry
- Readiness: NHS/Industry take-ups, exemplar projects, existing tools, datasets, open source
- Training: next generation clinical NLP leaders, ~~curriculum: undergraduate/graduate modules~~
- Usefulness: areas of applications
- ~~Opportunities, Barriers: TREs, information governance, trusts, responsibilities~~


## Information Collection and Data Extraction
We decided to start the information collection with identifying relevant projects funded by research councils and other major funders (e.g., charities) in the UK. The inclusion criteria include (a) develop or apply natural language processing technologies; (b) solve a clinical, public health or life science research problem that directly applicable to patient care.

<img src="/img/blog/ucnl-data-extraction.png" width="600"/>
<div class="img-cap">Figure 1. First step of information collection: identify relevant funded projects from UK research councils and other major funders</div>

The above figure illustrates the first step of information collection. We started with UK Research and Innovation (UKRI), which "*is a non-departmental public body of the Government of the United Kingdom that directs research and innovation funding, funded through the science budget of the Department for Business, Energy and Industrial Strategy*". UKRI provides an official API (Application Programming Interface) that allows efficient access (software based query and extraction) to funded projects from nine research councils including MRC, EPSC, BBSRC, ESRC and etc (see Figure 1 for the full list). Thirty-four combinations of keyword searches were used to query UKRI web service, which returned 97 unique projects. A manual assessment was then conducted to remove irrelevant ones according to the inclusion criteria. This left us with 60 valid projects. Similar process was conducted for NIHR, the National Institute for Health Research. NIHR is a UK government agency which funds research into health and care. Four keyword searches were used, which found 15 projects. After manual assessment, 11 projects were deemed as relevant. 
Searches to other funders including Wellcome Trust, Cancer Research UK and British Heart Foundation did not find relevant projects. 
Some of these funders do not provide sufficient metadata for their funded projects like abstracts. Therefore, some relevant projects might have been missed. Overall, we identified 71 relevant projects.

<img src="/img/blog/ucnl-data-expansion.png"/>
<div class="img-cap">Figure 2. Expand information from funded projects to associated persons, organisations, funders and publications.</div>

From the relevant projects, we further extended data extraction (see Figure 2) to include associated information including project metadata, related persons (such as principal investigators), organisations, funders, publications and other outputs (such as datasets or code repositories). For 89 organisations, we manually classified them into research, NHS and industry.

## Overall landscaping 

We created a graph representation of the collected data by associating funded projects (grant), investigators (person), involved institutions (organisation) and funding bodies (funder). 
This representation will allow us to obtain insights from the data via a range of analytics including visualisation, exploratory analysis and network analysis.

<div style="display: flex; margin: 10px">
<div style="flex: 50%; border-right: #c9dae1 solid 1px">
<p>Projects started before 2011, Total £:0.92m #grants:3 #org:6 </p>
<img src="/img/blog/ucnl-graph-2011.png"/>
</div>
<div style="flex: 50%; padding-left: 5px">
<p>Projects started before 2016, Total £:6.98m #grants:19 #org:32  </p>
<img src="/img/blog/ucnl-graph-2016b.png"/>
</div>
</div>


<div class="img-cap">Figure 3. Graph representations of clinical NLP landscape at two time points: 2011 (ten years ago) and 2016 (five years ago)</div>

Figure 4 shows the latest interactive graph representation of the UK's clinical NLP landscape as of data collected in October 2021. 

<div id="observablehq-chart-8b1cdf1d"></div>
<script type="module">
import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
import define from "https://api.observablehq.com/d/dba58bf36e70e95c.js?v=3";
new Runtime().module(define, name => {
  if (name === "chart") return new Inspector(document.querySelector("#observablehq-chart-8b1cdf1d"));
});
</script>
<div class="img-cap">Fingure 4. Clinical NLP Landscape as of 2021: an force-directed graph between grants, organisations, persons and funders. <p/>Total £:22.46m #grants:71 #org:89, funded by 7 funders.</div>

## Stakeholders
Let's look at the main stakeholders and associated trends in the last 15 years. 

### Key players
To identify important "players" in the clinical NLP field. We conducted centrality analysis on the graph representation of our collected data. 
Technically, the graph is an undirected with no weights on either nodes or links. We implemented five centrality metrics including degree,
betweeness, closeness, eigenvector, and page-rank. All of these are used for assess the importance of a node in a graph while different metrics look at slightly different aspects of topology characteristics. In this article, we report results using eigenvector based centrality. 
Eigenvector centrality measures the influence of a node in a graph. Nodes with high scores usually connects to nodes which have high scores themselves. This fits very well with our motivation to identify key players in the UK's clinical NLP landscape.

As we have multiple types of nodes in the graph, to make it easy to compare centrality scores of the same node types, we define 
**relative centrality score** as $$RCS(n, others) = \frac{centrality(n)}{median(\{centrality(x)| \forall x \in others\})}$$. 
It reads as centrality score of *n* relative to *others*.

### Funders
The table below lists all funders in our collected data, ordered by  Eigenvector centrality score relative to all funders.

<iframe width="100%" height="276" frameborder="0"
src="https://observablehq.com/embed/0aeef2a068c4e82f?cells=topFunderTable"></iframe>
<div class="img-cap">Table 1. All funders ranked by  Eigenvector Centrality scores relative to all Funders.</div>

Apparently, there are huge disparities between funders for supporting clinical NLP projects in the UK. 

> In particular, MRC and EPSRC play critical roles, which are >1.7 and >1.5 times respectively more influential than NIHR (the funder with the median centrality score in all funders). 

Innovate UK and NIHR have similar influences. It's interesting to see the largest amount of funding comes from NIHR, which achieved moderate influence in the clinical NLP landscape. The reason (of its lower influence per pound) could be twofold: (a) projects supported by NIHR are relative big projects in terms of funding scale - fewer links overall; (b) funded organisations and researchers do not overlap significantly with those supported by other key funders of MRC and EPSRC - separated from main component in the graph. Topologically, NIHR funded projects form a separate cluster (see Figure 4). We will come back to the connectivity analysis later.

### Organisations
<iframe width="100%" height="236" frameborder="0"
src="https://observablehq.com/embed/0aeef2a068c4e82f?cells=topOrgTable"></iframe>
<div class="img-cap sub">Table 2.a. Top 5 organisations</div>

<iframe width="100%" height="236" frameborder="0"
src="https://observablehq.com/embed/0aeef2a068c4e82f?cells=topNHSTable"></iframe>
<div class="img-cap sub">Table 2.b. Ranked list of all NHS Trusts.</div>

<iframe width="100%" height="236" frameborder="0"
src="https://observablehq.com/embed/0aeef2a068c4e82f?cells=topCompanyTable"></iframe>
<div class="img-cap sub">Table 2.c. Top 5 industry organisations</div>
<div class="img-cap">Table 2. Different types of Organisations ranked by Eigenvector centrality relative to all organisations.</div>

Table 2 shows the three ranked lists of organisations stratified by types. 
Unsurprisingly, the most influential organisations (of all types) are universities (see Table 2a). 
The only organisation in the top 10 list which is not a university is European Bioinformatics Institute (RCS=2.18, grant total=£2.12m). 
The combined influence of top 5 universities are >5 times than that of all four NHS Trusts involved (Table 2b), and near 4 times of that of top 5 industry institutions (Table 2c.
In fact, either of the top two universities (Manchester and UCL) has more influence than all NHS Trusts combined (which is 4.79). 

> The dominant influence of universities indicates clinical NLP is still a research-dominated area in the UK.

It is encouraging to see most NHS and industry organisations have a relative centrality score larger than one (i.e., higher than median centrality score), meaning they are involved in relatively high influential projects. In particular, out of all 89 organisations, Abtrace Limited (a startup company established in 2018 dedicated to AI in decision-making) is ranked 13th and Salford Royal NHS Foundation Trust (now Northern Care Alliance NHS Group, operating in the Great Manchester area) is ranked 14th. 

> These are promising signs that NLP technologies are starting to be taken up by the industry and healthcare service providers. 

### Individuals
The following figure illustrates the histogram of eigenvector scores of all persons in our graph. It shows a clear long-trail distribution.
One person has the highest score of 0.0067. The second highest is 0.0043. Three people have a score between 0.003 and 0.004. All others have a score lower than 0.003. Two of the top five individuals are from National Centre for Text Mining of University of Manchester. A project manager from Abtrace Limited is ranked the 5th.

![](/img/blog/uncl-persons-centrality-dist.png)
<div class="img-cap">Figure 5. Histogram of person nodes Eigenvector centrality scores: x-axis is the eigenvector centrality score and y-axis (log scale) is the number of people with certain scores.</div>

## Trends and Connectivity
### Increased Technology Maturity
Involvements of industry partners and deployments within health services are key indicators for the maturity of a technology. 
To obtain an understanding of the development of maturity of clinical NLP along the years, we group the organisations involved in funded projects into **NHS** and **Industry** and then look at the patterns of change in last 15 years. Figure 6 shows the trends on budgets of all projects, projects that involved NHS and proejects that involved industry in the last 15 years (3 year groups).

<iframe width="100%" height="376" frameborder="0"
src="https://observablehq.com/embed/0aeef2a068c4e82f?cells=barChart"></iframe>
<div class="img-cap">Figure 6. Trends in th 1ast 15 years on budgets of all projects, those involved NHS and those involved industry organisations</div>

It is clear that funding for clinical NLP in all three categories has increased significantly. It is particular encouraging to see NHS organisations are increasingly involved in this area since 2015. Industry involvements have increased >10 times from the 2015-2018 period to the 2018-2021 period.

> Particularly, industry involvements in all projects has leaped from less than 1/10 during 2015 to 2018 to more than 1/3 from 2018 on wards, indicating a possible increased technology maturity of clinical NLP in the last 3 years.

### Connectivity Analysis

To understand the interactions between groups in the community, it is important to know: (1) the key subgroups; and (d) how they connect with each other. 
From Figure 4, we can observe that there are three natural clusters in the graph. The biggest cluster contains **research** projects supported by funders like EPSC, MRC, BBSRC and ESRC.
The second cluster comes from NIHR funded projects, which are usually supposed to be more **translational**, meaning they are supposed to directly benefit patient care.
The third cluster are those funded by Innovate UK. Such projects are normally led by the industry, which are supposed to **produce products** that are ready for the end customers, i.e. health service providers like NHS in our case. Visually, the three clusters are weekly connected with each other. 

<iframe width="100%" height="236" frameborder="0"
src="https://observablehq.com/embed/0aeef2a068c4e82f?cells=kComponentTable"></iframe>
<div class="img-cap">Table 3. Funders contained in components of K-edge-connected analysis. Results for k in [1, 6].</div>

To quantify the strength of their connections, we conducted a connectivity analysis. The concept of connectivity is one of the basic concepts of graph theory: it meaures the minimum number of elements that need to be removed to separate the remaining nodes into two or more isolated subgraphs. In particular, we did k-edge-connectivity analysis - [*a connected graph is k-edge-connected if it remains connected whenever fewer than k edges are removed.*](https://en.wikipedia.org/wiki/K-edge-connected_graph)

Table 3 shows the changes of funders in components of the k-edge-connected results. When k=2, Innovative UK is separated from the main cluster. 
> This means the Innovative UK and its funded projects are very weakly linked with other funders and their funded projects/people - only one edge to be specific.

When k=3, the whole subgraph of Innovative UK disappears, meaning the connectivity within its own cluster is also weak. 
For the main cluster where all other funders reside, the connectivity is not strong between all: ESRC disconnected at 4 and NIHR disconnected at 5.
EPSRC and MRC forms the core which keeps connection until k reaches 15. 
> This shows a pretty strong connectivity among research projects funded by MRC and EPSRC.

Table 4 lists all the entities (grants, organisations, funders and persons) within the 6-edge-connected component, representing the core network.
<iframe width="100%" height="406" frameborder="0"
src="https://observablehq.com/embed/0aeef2a068c4e82f?cells=coreEntitiesTable"></iframe>
<div class="img-cap">Table 4. All entities within the 6-edge-connected component.</div>

So far, we have seen the connectivity between Innovative UK, NIHR and other funders are weak in the most recent data collected by this study. Let's look back in about one year:
 the interactive figure below shows what the whole graph looks like on 1st June, 2020 (data related to projects started on or before this date).

<div id="observablehq-chart202006-a5f35208"></div>
<script type="module">
import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
import define from "https://api.observablehq.com/d/dba58bf36e70e95c.js?v=3";
new Runtime().module(define, name => {
  if (name === "chart202006") return new Inspector(document.querySelector("#observablehq-chart202006-a5f35208"));
});
</script>
<div class="img-cap">Graph of projects started on or before 1st June 2020 and their associated entities - zoom out to see disjointed clusters</div>

It shows NIHR, Innovative UK and other funders funded projects are totally separated in about one year ago.
> This illustrates since June 2020 connections between research, innovation and translation have been established. However, so far, the connectivity between the three are still pretty weak.

## Training and Next Generation Clinical NLP Leaders
We analysed the studentship projects (i.e., funded via doctoral training programmes) in collected data to understand the trends of clinical NLP related PhD projects in the last years. Figure 7 below shows four snapshots for funded studentship projects for those started by 2016, 2017, 2019 and 2021 respectively. 
> It is worth mentioning that there was not a single studentship project related to clinical NLP before September 2016, while NLP has been used in some NHS Trusts for more than 7 years (e.g., South London and Maudsley started NLP in 2009).
<div style="display: flex; margin: 10px">
<div style="flex: 40%;vertical-align: bottom">
<img src="/img/blog/ucnl-studentship-2016.png"/>
First project was funded by MRC, led by Edinburgh and started in 2016.
</div>
<div style="flex: 60%; padding-left: 5px;">
<img src="/img/blog/ucnl-studentship-2017.png"/>
One year later, in 2017, there were three projects: two new institutions of Birmingham and St George's and one new funder - EPSRC - joined the party. 
</div>
</div>
<div style="padding: 20px; border-top: solid 1px #cfcfcf">
<img src="/img/blog/ucnl-studentship-2019.png"/>
Another two years saw consistent increasing in PhD projects (8 in total). Sheffield got two projects and Warwick got one, while Edinburgh and Birmingham each got one new project.
</div>
<div style="padding: 20px; border-top: solid 1px #cfcfcf">
<img src="/img/blog/ucnl-studentship-2021.png"/>
Until October 2021, there are total 16 funded studentship projects relevant to clinical NLP. Ten were funded by EPSRC and five by MRC. ESRC funded a project led by Cambridge. Institutions with more than one studentships include UCL, Edinburgh, Imperial, Birmingham and Sheffield.
</div>
<div class="img-cap"> Figure 7. The development of studentship projects from 2016 to 2021.</div>

> Since 2016, the studentship projects have increased from just one to sixteen across fourteen institutions. The patterns of continuous increase and wide-spreading are encouraging. 

Such developments are probably backed by recent UKRI funded Centres for Doctoral Training focusing on AI technologies in health care ([https://www.turing.ac.uk/work-turing/studentships/centres-doctoral-training-cdts](https://www.turing.ac.uk/work-turing/studentships/centres-doctoral-training-cdts)). NLP technologies have seen continuous interest in the research community and increasing demands from the NHS to deal with backlog and increase service efficiency and efficacy. It is reasonable to expect continuous increase in the number of studentships in the coming years. 

## Usefulness - areas of applications
Figure 8 below shows the distribution of disease areas of funded projects. This is derived from funder provided metadata - health category. Note that only 23 out of 71 projects have such data. Beside generic areas, cancer, neurological and mental health are the most investigated areas.
![Health categories](/img/blog/ucnl-health-cats.png)
<div class="img-cap"> Figure 8. Health categories as specified by the funders' metadata.</div>

Figure 9 illustrates the research subjects of funded projects. Again, it uses the metadata from the funders and only 12 projects have such data. Out of all subjects, the most frequently studied is Information and Communication Technologies (9/12), followed by "Tools, technologies and methods" (5/12) and "Linguistics". Note that one project might have multiple research subjects (2/12).
![Research subjects](/img/blog/ucnl-research-subjects.png)
<div class="img-cap"> Figure 9. Research subjects as specified by the funders' metadata.</div>

To get a detailed analysis on whole set of projects, we conducted a Latent Dirichlet Allocation (LDA) analysis on the abstracts of all 71 projects. This is to identify natural **topics** from all these projects.
![LDA results](/img/blog/ucnl-lda-result.png)
<div class="img-cap"> Figure 10. Latent Dirichlet Allocation results. Topic 6 - self, cognitive change, awareness, Alzheimer, detection. </div>

Table below shows the nine topics identified by LDA on 71 projects' abstracts.

| Topic   | Application area terms                                     | Method terms           |
|---------|------------------------------------------------------------|------------------------|
| topic 1 | social, clinical, self assessment,   risk                  | systematic             |
| topic 2 | RNA, seq, gene, evidence, effectiveness, molecule          | literature             |
| topic 3 | clinical, diagnosis, cancer, health record, subtype        | semantic               |
| topic 4 | sudden, death, big, digital, service                       | ontology               |
| topic 5 | phenotype, review, mining, bias, disease                   | literature, systematic |
| topic 6 | self, cognitive change, awareness,   Alzheimer, detection |                        |
| topic 7 | virus, model, decision, uncertainty                        | semantic, transformer  |
| topic 8 | NOAF, identifier, ICU, biology,   organism, molecule       |                        |
| topic 9 | subtype, Parkinson, functional, cognitive                  |                        |