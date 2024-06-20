---
layout: default
title: Open Science in Automotive User Research
---

<style>
table {
    width: 100%;
    table-layout: fixed;
    overflow: auto;
}
th, td {
    padding: 0.5rem 1rem;
    border: 1px solid #ccc;
}
</style>

# Open Science in Automotive User Research

Open Science principles are critical in advancing transparency, collaboration, and accessibility in research. By embracing these values, we aim to create a more inclusive and dynamic research environment, particularly within the automotive user research community. This initiative reflects our commitment to driving forward the development of open, user-centered automotive technologies and services, ensuring that knowledge and findings are shared openly to benefit the broader community.

## Why Open Science?

The pursuit of Open Science is essential for several reasons:

- **Accelerating Knowledge Dissemination:** Open Science practices ensure that research findings are shared more broadly and quickly, facilitating faster advancements in the field.
- **Enhancing Collaboration:** By making research data and methodologies openly available, we foster an environment where researchers can easily collaborate, building upon each other's work to push the boundaries of knowledge.
- **Promoting Transparency and Reproducibility:** Open access to research findings and data supports the verification of results, enhancing the credibility and reliability of research within our community.


## Towards Open Science

**Every step** toward greater transparency in research is valuable, contributing incrementally to the overall integrity and reproducibility of scientific work. It's important to recognize and celebrate each step taken, even if complete openness is not immediately achieved. Here are three levels of engagement with open science practices:

- **Level 1**:
  - **Document methods and results**: Even if data cannot be shared, detailed documentation of research methods and results can be invaluable.
  - **Acknowledge limitations**: Clearly state any restrictions on data sharing and transparency, explaining the reasons behind them.

- **Level 2**:
  - **Share data when possible**: When permissible, share data in a trusted repository, ensuring it is de-identified and secure.
  - **Use open-access platforms**: Publish findings in open-access journals or platforms to make the research accessible to a broader audience.

- **Level 3**:
  - **Full data and code availability**: Share all research data, code, and materials necessary to replicate the study.
  - **Engage in pre-registration**: Register study protocols in advance to enhance the credibility of the research.




## Practical Tips for Embracing Open Science

Following the guidelines we shared for the [AutomotiveUI '24 conference](https://www.auto-ui.org/24/authors/open-science/), here are practical tips to incorporate Open Science into your research workflow:

### Data Sharing and Management

There are many places where we can publish open access artifacts. It is good practice to keep your data on a FAIR platform/repository. Here are some examples (updated June 2024):

1. **[ACM Digital Library](https://dl.acm.org)** (FAIR): AutoUI is an ACM conference, and the platform allows the sharing of (small) supplementary material with the publication.
2. **[OSF](https://osf.io)** (FAIR): Allows to make repos anonymous for review, which can be handy for the submission process. It is a ‘swiss knife’ for publishing artifacts in open access, and the platform allows a great level of flexibility. File versioning is straightforward, and OSF also allows you to pre-register your study. It is also easy to make your material anonymous for the review process.
3. **[Zenodo](https://zenodo.org)** (FAIR): Data is stored at CERN, which is reliable. It is becoming a common place to share data, which may make it user-friendly. They accept up to 50GB per dataset with an option to have multiple datasets.
4. **[GitHub](https://github.com)** (**not** FAIR) Everyone knows how to navigate around a repo on GitHub, which can be an advantage for outreach. But it is not FAIR. What can be practiced is to provide a link to the active project in the manuscript, and then still upload materials to a FAIR platform for reproducibility.
5. **[4TU.ResearchData](https://data.4tu.nl)** (FAIR): Local storage for the technical universities of the Netherlands. They do quite a good job of making the management of datasets easy. Likely, there is a similar portal in your institution/country.



### Open Access Publications

- **Choose Open Journals:** When publishing your findings, opt for journals that offer open access, making your research available to all. Avoid [Predatory Journals](https://beallslist.net/).
- **Preprints:** Consider posting preprints of your research to platforms like [arXiv](https://arxiv.org/) or [bioRxiv](https://www.biorxiv.org/) to share your findings ahead of journal publication.

### Transparency in Methodology

- **Code Sharing:** Use FAIR platforms/repositories (see above) to share the code used in your research, including analysis scripts and software developed as part of your work.
- **Detailed Documentation:** Ensure that your methodologies are thoroughly documented and shared, allowing others to replicate or build upon your work.

## Related Works and Resources

Here, we provide a dynamically updated table of related works, categorized by criteria such as datasets, simulation software, models, and surveys, to facilitate easy access to a wealth of resources that can support your Open Science endeavors.

We **encourage authors of papers with openly available materials to create a Pull request** to add their work. 
Add your work here: [Related Works CSV](https://raw.githubusercontent.com/AutoUI-Open-Data-Initiative/autoui-open-data-initiative.github.io/master/_data/related_works.csv).
Category must be one of [Dataset, Software, Model, Survey].
We will check the entry and approve it in a timely manner. 


### Datasets

| Category    | Title              | Author   | Year | Link |
{% assign dataset = site.data.related_works | where: "Category", "Dataset" | sort: 'Year' %}
{% for item in dataset %}
| {{ item.Category }} | {{ item.Title }} | {{ item.Author }} | {{ item.Year }} | [Link]({{ item.Link }}) |
{% endfor %}



<table border="1">
  <thead>
    <tr>
      {% for header in site.data.related_works[0] %}
        <th>{{ header[0] }}</th>
      {% endfor %}
    </tr>
  </thead>
  <tbody>
    {% for row in site.data.data %}
      <tr>
        {% for cell in row %}
          <td>{{ cell }}</td>
        {% endfor %}
      </tr>
    {% endfor %}
  </tbody>
</table>


### Software

| Category    | Title              | Author   | Year | Link |
{% assign simulationsoftware = site.data.related_works | where: "Category", "Software" | sort: 'Year' %}
{% for item in simulationsoftware %}
| {{ item.Category }} | {{ item.Title }} | {{ item.Author }} | {{ item.Year }} | [Link]({{ item.Link }}) |
{% endfor %}

### Models

| Category    | Title              | Author   | Year | Link |
{% assign models = site.data.related_works | where: "Category", "Model" | sort: 'Year' %}
{% for item in models %}
| {{ item.Category }} | {{ item.Title }} | {{ item.Author }} | {{ item.Year }} | [Link]({{ item.Link }}) |
{% endfor %}

### Surveys

| Category    | Title              | Author   | Year | Link |
{% assign surveys = site.data.related_works | where: "Category", "Survey" | sort: 'Year' %}
{% for item in surveys %}
| {{ item.Category }} | {{ item.Title }} | {{ item.Author }} | {{ item.Year }} | [Link]({{ item.Link }}) |
{% endfor %}

### Other

| Category    | Title              | Author   | Year | Link |
{% assign excluded_categories = "Survey,Model,Software,Dataset" | split: "," %}
{% for item in site.data.related_works %}
  {% unless excluded_categories contains item.Category %}
    | {{ item.Category }} | {{ item.Title }} | {{ item.Author }} | {{ item.Year }} | [Link]({{ item.Link }}) |
  {% endunless %}
{% endfor %}






## Paper and Workshop

If you found this information useful, consider looking at and citing:

```
@inproceedings{ebel2024changing,
  title={Changing Lanes Toward Open Science: Openness and Transparency in Automotive User Research},
  author={Ebel, Patrick and Bazilinskyy, Pavlo and Colley, Mark and Goodridge, Courtney and Hock, Philipp and Janssen, Christian P. and Sandhaus, Hauke and Srinivasan, Aravinda Ramakrishnan and Wintersberger, Philipp},
  booktitle={16th International Conference on Automotive User Interfaces and Interactive Vehicular Applications (AutomotiveUI '24)},
  pages={17},
  year={2024},
  address={Stanford, California, USA},
  month={sep},
  publisher={ACM},
  location={New York, NY, USA},
  note={Conditionally accepted}
}
```

Also see the 2023 workshop [website](https://autouimodelingws.jimdosite.com/) for more information.




## Conclusion

Embracing Open Science is a journey that requires commitment, collaboration, and a willingness to share and learn from one another. We invite the automotive user research community to join us in this endeavor, working together to advance our field in a way that is open, inclusive, and transparent.












