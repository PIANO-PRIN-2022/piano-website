---
title: "About"
navigable: true
nav_order: 2
---

PIANO is a research project funded by [Next Generation EU](https://ext-generation-eu.europa.eu/index_en){:target="_blank"}
as part of the 2022 edition of Italian Research Projects of National Relevance (PRIN 2022),
via the initiative [Italia Domani](https://www.italiadomani.gov.it/content/sogei-ng/it/en/home.html){:target="_blank"}.


## Motivation
{: #motivation}

The online spread of toxic speech hinders the exchange and fruition of information, increases radicalization, and may even cause offline harms.
To mitigate toxicity, online platforms enforce moderation interventions, such as warning messages, to discourage toxic behaviors and the removal of toxic content and users.
Until now, however, these have not significantly reduced online toxicity.
So far, all moderation interventions have followed a “one-size-fits-all” approach, where each intervention is applied in the same way for all users.
That is to say, personalization in online moderation remains an unexplored strategy.


## Approach
{: #approach}

PIANO proposes a pioneering approach to online moderation by designing personalized moderation interventions against online toxicity.
PIANO will adopt a cross-disciplinary approach grounded on psychology and on machine learning and AI techniques to achieve the project's Research Objectives (ROs).
To this end, our multidisciplinary team will collaborate on user modeling, producing methods for inferring user personality traits based on public traces of online activity.

We will first use knowledge of the user traits and theories from personality psychology and past user behavior to describe users (**RO1**: User Modeling), which will then inform a process for crafting multiple text-based interventions tailored to the personality of the users to which it will be applied (**RO2**: Personalization).
The end result of PIANO will be a set of theoretical and methodological models for suggesting the best intervention for any given toxic user.


## Consortium
{: #consortium}

Our multidisciplinary consortium is composed of three research units:

{% for partner in site.data.partners %}
  - [{{ partner.unit.name }}]({{ partner.unit.url }}){:target="_blank"}, {{ partner.fullname }} (**{{ partner.name | upcase }}**)
{%- endfor %}

{% for partner in site.data.partners %}
  <br>
  {% include partner_img.html partner = partner %}

  {{ partner.unit.description }}
{%- endfor %}


## Workplan
{: #workplan}

The project started in October 2023, it has an expected duration of two years, and consists of five work packages (WPs).

{% for wp in site.data.workplan %}

### {{ wp.name }}: {{ wp.title }}

_Leader:_ {{ wp.leader | upcase }}

{{ wp.objective }}

  {% for task in wp.tasks -%}
- **{{ task.name }}**: {{ task.title }}
  {% endfor %}

{%- endfor %}


## Contact
{: #contact}

- [Stefano Cresci](https://www.iit.cnr.it/en/stefano.cresci/){:target="_blank"} <small>(Principal Investigator)<small>
- Istituto di Informatica e Telematica (IIT)
- Consiglio Nazionale delle Ricerche (CNR)
- Area della Ricerca
- Via Giuseppe Moruzzi, 1
- 56124 Pisa – Italy
{: #about-contact-list}