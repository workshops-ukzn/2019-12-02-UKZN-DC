---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "dc"    # what kind of Carpentry (must be either "lc" or "dc" or "swc")
venue: "UKZN, Westville Campus"        # brief name of host site without address (e.g., "Euphoric State University")
address: "Seminar Room 5, Govan Mbeki, Research Office, Westville Campus"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "za"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/ISO_639-1)
latlng: "-29.818203, 30.945906"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use https://www.latlong.net/)
humandate: "2nd and 3rd December, 2019"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "8:30 - 16:30"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2019-12-02      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2019-12-03        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Moses Okpeku", "Matthew Adeleke", "Tadiwanashe Gutsa" , "Oluwafisayo Kaka"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Naomi Kingu, Ayodeji Ogunode"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["tadigutsah@gmail.com, oluwafisayo.kaka@gmail.com"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:     https://pad.carpentries.org/2019-12-02-UKZN-DC        # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

<h2 id="general">General Information</h2>
Data Carpentry’s aim is to teach researchers basic concepts, skills, and tools for working
with data so that they can get more done in less time, and with less pain. This workshop
teaches data management and analysis for genomics research including: 
best practices for organization of bioinformatics projects and data, use of command-line 
utilities, use of command-line tools to analyze sequence quality and
perform variant calling, and connecting to and using cloud computing. This workshop is designed to 
be taught over two full days of instruction. 


<p style = "color:red;"><strong>Registration:</strong> Please complete the online registration form at <a href="https://forms.gle/EmrC8S5e3ERuDKZV7">https://forms.gle/EmrC8S5e3ERuDKZV7</a>. Limited space is available. The workshop is free to attend but a R500 no-show fee will be payable by a registered participant who does not show up to the workshop without giving the workshop organisers at least 3 days notice.
</p>

<blockquote>The workshop is part of a series of Digital Literacy workshops supported by the Big Data and Informatics Research Flagship and funded through the University Capacity Development Programme (UCDP) at UKZN.</blockquote>

{% comment %}
  AUDIENCE

  Explain who your audience is.  (In particular, tell readers if the
  workshop is only open to people from a particular institution.
{% endcomment %}
{% if page.carpentry == "swc" %}
  {% include sc/who.html %}
{% elsif page.carpentry == "dc" %}
  {% include dc/who.html %}
{% elsif page.carpentry == "lc" %}
  {% include lc/who.html %}
{% endif %}


{% comment %}
  SPECIAL REQUIREMENTS

  Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Requirements:</strong> Participants must bring a laptop with a
  Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) that they have administrative privileges
  on. They are also required to abide by
  {% if page.carpentry == "swc" %}
  Software Carpentry's
  {% elsif page.carpentry == "dc" %}
  Data Carpentry's
  {% elsif page.carpentry == "lc" %}
  Library Carpentry's
  {% endif %}
  <a href="{{site.swc_site}}/conduct.html">Code of Conduct</a>.
</p>



{% comment %}
  CONTACT EMAIL ADDRESS

  Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
    {% for email in page.email %}
      {% if forloop.last and page.email.size > 1 %}
        or
      {% else %}
        {% unless forloop.first %}
        ,
        {% endunless %}
      {% endif %}
      <a href='mailto:{{email}}'>{{email}}</a>
    {% endfor %}
  {% else %}
    to-be-announced
  {% endif %}
  for more information.
</p>

<hr/>
{% comment %}
  SCHEDULE

  Show the workshop's schedule.  Edit the items and times in the table
  to match your plans.  You may also want to change 'Day 1' and 'Day
  2' to be actual dates or days of the week.
{% endcomment %}
<h2 id="schedule">Schedule</h2>

{% if page.carpentry == "dc" %}
  {% schedule.html %}
{% endif %}

> ## Getting Started
>
> This lesson assumes that learners have no prior experience with the tools covered in the workshop. 
> However, learners are expected to have some familiarity with biological concepts,
> including the 
> concept of genomic variation within a population. Participants should bring their own laptops and plan to participate actively. 
> 
> To get started, follow the directions in the [Setup](setup.html) tab to 
> get access to the required software and data for this workshop.
> 
{: .prereq}

> ## Data
> 
> This workshop uses data from a long term evolution experiment published in 2016: [Tempo and mode of genome evolution in a 50,000-generation experiment](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4988878/) by Tenaillon O, Barrick JE, Ribeck N, Deatherage DE, Blanchard JL, Dasgupta A, Wu GC, Wielgoss S, Cruveiller S, Médigue C, Schneider D, and Lenski RE. (doi: 10.1038/nature18959)
>
> All of the data used in this workshop can be [downloaded from Figshare](https://figshare.com/articles/Data_Carpentry_Genomics_beta_2_0/7726454). 
> More information about this data is available on the [Data page](https://datacarpentry.org/organization-genomics/data/).
{: .prereq} 


# Workshop Overview 

| Lesson    | Overview |
| ------- | ---------- |
| [Project organization and management](https://datacarpentry.github.io/organization-genomics/) | Learn how to structure your metadata, organize and document your genomics data and bioinformatics workflow, and access data on the NCBI sequence read archive (SRA) database.|
| [Introduction to the command line](https://datacarpentry.github.io/shell-genomics/) |  Learn to navigate your file system, create, copy, move, and remove files and directories, and automate repetitive tasks using scripts and wildcards. |
|[Data wrangling and processing](https://datacarpentry.github.io/wrangling-genomics/) | Use command-line tools to perform quality control, align reads to a reference genome, and identify and visualize between-sample variation. |
|[Introduction to cloud computing for genomics](http://www.datacarpentry.org/cloud-genomics/) | Learn how to work with Amazon AWS cloud computing and how to transfer data between your local computer and cloud resources. 



{% comment %}
  Collaborative Notes

  If you want to use an Etherpad, go to

      http://pad.software-carpentry.org/2019-12-02-UKZN-DC

  where 'YYYY-MM-DD-site' is the identifier for your workshop,
  e.g., '2015-06-10-esu'.
{% endcomment %}
{% if page.collaborative_notes %}
<p id="collaborative_notes">
  We will use this <a href="{{page.collaborative_notes}}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
{% endif %}


# Optional Additional Lessons

| Lesson | Overview |
| ------- | -------- |
| [Intro to R and RStudio for Genomics](https://datacarpentry.org/genomics-r-intro/) | Use R to analyze and visualize between-sample variation. |

# Teaching Platform
This workshop is designed to be run on pre-imaged Amazon Web Services (AWS)
instances. All the software and data used in the workshop are hosted on an Amazon Machine Image (AMI).
If you want to run your own instance of the server used for this workshop, follow the directions in the [Setup](setup.html) tab. 

