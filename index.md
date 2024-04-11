---
layout: default
title: Open Science in Automotive User Research
---

# Open Science in Automotive User Research

Open Science principles are critical in advancing transparency, collaboration, and accessibility in research. By embracing these values, we aim to create a more inclusive and dynamic research environment, particularly within the automotive user research community. This initiative reflects our commitment to driving forward the development of open, user-centered automotive technologies and services, ensuring that knowledge and findings are shared openly to benefit the broader community.

## Why Open Science?

The pursuit of Open Science is essential for several reasons:

- **Accelerating Knowledge Dissemination:** Open Science practices ensure that research findings are shared more broadly and quickly, facilitating faster advancements in the field.
- **Enhancing Collaboration:** By making research data and methodologies openly available, we foster an environment where researchers can easily collaborate, building upon each other's work to push the boundaries of knowledge.
- **Promoting Transparency and Reproducibility:** Open access to research findings and data supports the verification of results, enhancing the credibility and reliability of research within our community.

In light of these benefits, we have taken steps to integrate Open Science principles into our research practices, aiming to lead by example within the automotive user research community.

## Practical Tips for Embracing Open Science

Following the guidelines we shared for the [AutomotiveUI '24 conference](https://www.auto-ui.org/24/authors/open-science/), here are practical tips to incorporate Open Science into your research workflow:

### Data Sharing and Management

- **Use Repositories:** Leverage platforms like Zenodo or the Open Science Framework (OSF) to share your datasets, ensuring they are accessible and citable.
- **Adopt FAIR Principles:** Ensure your data is Findable, Accessible, Interoperable, and Reusable to maximize its value to the community.

### Open Access Publications

- **Choose Open Journals:** When publishing your findings, opt for journals that offer open access, making your research available to all.
- **Preprints:** Consider posting preprints of your research to platforms like arXiv or bioRxiv to share your findings ahead of journal publication.

### Transparency in Methodology

- **Code Sharing:** Use platforms like GitHub to share the code used in your research, including analysis scripts and software developed as part of your work.
- **Detailed Documentation:** Ensure that your methodologies are thoroughly documented and shared, allowing others to replicate or build upon your work.

## Related Works and Resources

Here, we provide a dynamically updated table of related works, categorized by criteria such as datasets, simulation software, models, and surveys, to facilitate easy access to a wealth of resources that can support your Open Science endeavors.

### Datasets

| Category    | Title              | Author   | Year | Link |
{% assign dataset = site.data.related_works | where: "Category", "Dataset" | sort: 'Year' %}
{% for item in dataset %}
| {{ item.Category }} | {{ item.Title }} | {{ item.Author }} | {{ item.Year }} | [Link]({{ item.Link }}) |
{% endfor %}

### Software

| Category    | Title              | Author   | Year | Link |
|-------------|--------------------|----------|------|------|
{% assign simulationsoftware = site.data.related_works | where: "Category", "Software" | sort: 'Year' %}
{% for item in simulationsoftware %}
| {{ item.Category }} | {{ item.Title }} | {{ item.Author }} | {{ item.Year }} | [Link]({{ item.Link }}) |
{% endfor %}

### Models

| Category    | Title              | Author   | Year | Link |
|-------------|--------------------|----------|------|------|
{% assign models = site.data.related_works | where: "Category", "Model" | sort: 'Year' %}
{% for item in models %}
| {{ item.Category }} | {{ item.Title }} | {{ item.Author }} | {{ item.Year }} | [Link]({{ item.Link }}) |
{% endfor %}

### Surveys

| Category    | Title              | Author   | Year | Link |
|-------------|--------------------|----------|------|------|
{% assign surveys = site.data.related_works | where: "Category", "Survey" | sort: 'Year' %}
{% for item in surveys %}
| {{ item.Category }} | {{ item.Title }} | {{ item.Author }} | {{ item.Year }} | [Link]({{ item.Link }}) |
{% endfor %}

### Other

| Category    | Title              | Author   | Year | Link |
|-------------|--------------------|----------|------|------|
{% assign excluded_categories = "Survey,Model,Software,Dataset" | split: "," %}
{% for item in site.data.related_works %}
  {% unless excluded_categories contains item.Category %}
    | {{ item.Category }} | {{ item.Title }} | {{ item.Author }} | {{ item.Year }} | [Link]({{ item.Link }}) |
  {% endunless %}
{% endfor %}



We encourage authors of papers with openly available materials to create a Pull request so that their work can be added.
Category must be one of [Dataset, Software, Model, Survey].

## Conclusion

Embracing Open Science is a journey that requires commitment, collaboration, and a willingness to share and learn from one another. We invite the automotive user research community to join us in this endeavor, working together to advance our field in a way that is open, inclusive, and transparent.

For more information, updates, and resources, keep an eye on this page and our upcoming publications and workshops dedicated to Open Science in automotive user research.

[Link to Paper and Workshop: To be updated once available to maintain anonymity during the review process.]

