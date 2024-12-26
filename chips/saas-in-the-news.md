# SaaS In the News

This page collects links to interesting articles relevant to the course topics, organized by which chapter/topic each is relevant to and sorted most-recent-first within each topic. Links to articles, videos, etc. does not imply endorsement by us of their points of view, nor do we have any formal connection to the authors unless otherwise stated; we just think these are relevant to software engineering and useful in helping to put in context some of the material taught in the course.

Evergreen articles—generally relevant and not tied to a specific event—have _<mark style="color:green;">**bold italic green titles**</mark>_**.**

## General

[The Unix Chainsaw](https://www.youtube.com/watch?v=ZQnyApKysg4) \[video]: a great explanation of why Unix command-line skills are so valuable for developers, and a great illustration of the "Unix philosophy" of combining small specialized tools. One of the examples is a mini-master-class in using the entire Unix environment as your IDE.

## 1 Introduction to Software as a Service, Agile Development, and Cloud Computing

_<mark style="color:green;">**June 2023:**</mark>_ [How NASA Writes Space-Proof Code](https://www.youtube.com/watch?v=GWYhtksrmhE) \[video]. The ultimate plan-and-document organization writes code for systems that may be millions of miles away and/or unreachable when something goes wrong. How do they do it?

_<mark style="color:green;">**November 2023**</mark>_: [Why do mainframes still exist? What's inside one?](https://www.youtube.com/watch?v=ouAG4vXFORc) \[video] A theme of this class is that good design is about choices, and while SaaS+Agile+Cloud is a great choice for many apps, some apps have quite different requirements. This video, replete with technical detail, is a fascinating look at the latest IBM zSeries mainframes—their design, including AI acceleration hardware; redundancy and reliability; and the kinds of apps that need those affordances.

_<mark style="color:green;">**October 2023**</mark>_: [The IRS is rolling out its (new) free tax-filing tool, and surprisingly, it's great](https://www.fastcompany.com/91178532/the-irs-is-rolling-out-its-free-tax-filing-tool-to-30-million-americans-and-surprisingly-its-great). Chapter 1 of ESaaS tells the dismal story of the disastrous 2013 rollout of Healthcare.gov, the US Government's health insurance portal, which was to be a signature achievement of President Barack Obama's administration. We also presented some opinionated commentary about whether things might have turned out better if government software efforts were developed with more of the Agile practices in mind, rather than the BDUF approach that had characterized most government software procurement. Fast forward ten years, and I guess the government took our advice :-)  The Internal Revenue Service (the tax-collecting agency of the US Government) worked with the [US Digital Service](https://usds.gov) and with [18F](https://18f.gsa.gov), an organization founded by several Presidential Innovation Fellows during the Obama administration to modernize US Government IT by bringing in the best practices of private industry.  They followed some of the most important Agile practices: they allowed potential users to play with different mockups, observing their behavior and putting the best ideas into the prototype; they included the customer in continuous refinements of the design; they started with a small deployment to find and fix bugs and make improvements before scaling up. As a result, Direct File processed more than 140,000 returns during its first year, exceeding its goal of 100,000, and suffered no outages in the process. (By comparison, H\&R Block, one of the largest private-sector providers of tax services, suffered some outages on tax day.) A General Services Administration survey found that more than 90% of users who tried Direct File rated it “excellent” or “above average,” and  86% of users said the experience increased their trust in the IRS, a government agency not traditionally known for high user confidence or loyalty.

_<mark style="color:green;">**December 2023**</mark>_: [What Do ChatGPT and AI-based Automatic Program Generation Mean for the Future of Software?](https://cacm.acm.org/blogcacm/what-do-chatgpt-and-ai-based-automatic-program-generation-mean-for-the-future-of-software/) Distinguished software engineer and professor Bertrand Meyer argues that while LLMs will generate better and better code, some of the key activities that differentiate _software engineering_ from _programming,_ such as requirements generation, specification, and verification, will only increase in importance.

_<mark style="color:green;">**December 2024**</mark>_: Addy Osmani [observes](https://addyo.substack.com/p/the-70-problem-hard-truths-about) (as have many others) that experienced and novice developers use generative AI in very different ways to assist in software development, often with very different outcomes.

## 2 How to Learn a New Language

## 3 SaaS Application Architecture: Microservices, APIs, and REST

September 2023: [Google's widely-opposed ad platform, "the privacy sandbox," launches in Chrome](https://arstechnica.com/gadgets/2023/09/googles-widely-opposed-ad-platform-the-privacy-sandbox-launches-in-chrome/). Cookies have a (well earned) bad reputation for being used to track users across websites, but rather than a tracking-free experience, Google has been pushing an alternative model that the Electronic Frontier Foundation calls "[a terrible idea](https://www.eff.org/deeplinks/2021/03/googles-floc-terrible-idea)." But because it'll be built into Chrome, a lot of users will probably unknowingly opt in by default.

## 4 SaaS Framework: Rails as a Model--View--Controller Framework

## 5 SaaS Framework: Advanced Programming Abstractions for SaaS

## 6 Mobile and Desktop SaaS Clients: JavaScript Introduction

## 7 Requirements: BDD and User Stories

## 8 Testing: Test-Driven Development

February 2024: [Self-pay gas station pumps break across NZ as software can’t handle Leap Day](https://arstechnica.com/gadgets/2024/02/leap-year-glitch-broke-self-pay-pumps-across-new-zealand-for-over-10-hours/). We thought this was amusing since a very similar bug is used as the example of TDD and debugging (the leap year problem with Microsoft Zune music player).

## 9 Software Maintenance: Enhancing Legacy Software Using Refactoring and Agile Methods

_<mark style="color:green;">**February 2023**</mark>_: [The Airline Industry's Problem With Absolutely Ancient IT](https://www.youtube.com/watch?v=1-m_Jjse-cs) \[video]. The catastrophic meltdown of airlines at Christmas 2022, once the terrible weather had subsided, was largely an IT problem. Here's a lesson in what happens when legacy systems are ignored for too long rather than updated incrementally.

## 10 Agile Teams

## 11 Design Patterns for SaaS Apps

## 12 Dev/Ops

_<mark style="color:green;">**January 2019**</mark>_: [SQL Is No Excuse to Avoid Dev/Ops](https://cacm.acm.org/practice/sql-is-no-excuse-to-avoid-devops/). Besides busting the myth that "heavyweight" SQL databases (vs. NoSQL stores) somehow get in the way of agile deployment due to schema-management concerns, this practitioner-focused article basically walks through a feature-flagged, schema-versioned approach to agile dev/ops very close to the one espoused by ESaaS, including how to test such changes in CI before production deployment.

November 2023: [Highly invasive backdoor snuck into open source packages targets developers. ](https://arstechnica.com/security/2023/11/developers-targeted-with-malware-that-monitors-their-every-move/)Typical modern software projects rely on hundreds of open source libraries. But how do you know there isn't malicious code lurking in those libraries?

July 2024:\
[How Crowdstrike brought worldwide IT to a halt](https://www.youtube.com/watch?v=wAzEJxOo1ts) \[video]. A good explanation by a Windows developer of what specific properties of this anti-malware product allowed it to compromise so many systems in such a thorough way.&#x20;

