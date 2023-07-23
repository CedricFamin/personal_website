---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin

  - block: markdown
    id: skills
    content:
      title: Skills
      subtitle: Keep in mind that this is just a glimpse of my capabilities :)
      text: |2- 
        ### General
        {{< gallery album="skills" resize_options="96x96" >}}

        <hr />

        ### Programming
        {{< gallery album="skills_programming" >}}

        <hr />

        ### AWS Cloud
        {{< gallery album="skills_aws" >}}

  - block: experience
    id: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Senior Quality Assurance Engineer
          company: Ubisoft
          company_url: ''
          company_logo: org-ubisoft
          location: France
          date_start: '2019-02-15'
          date_end: '2023-02-15'
          description: |2-
              Create automatic tests thanks to an internal tools based on Gherkin synthax. Owner of the strategy & implementation of tests for two AAA games.

              Responsabilities includes:

              * Implementing in-engine feature to enable external game manipulation.
              * Managing machines, install all requirements to run tests.
              * Creating a weekly custom report (Python + plotly -> HTML).
              * Monitoring tests result, first level support.
              * Developing the test strategy with QA owners.
              * Defining the need with game designers, gameplay programmers ...
              * Managing & train newcomers.

        - title: Senior Data Engineer
          company: Ubisoft
          company_url: ''
          company_logo: org-ubisoft
          location: France
          date_start: '2016-01-01'
          date_end: '2019-02-15'
          description: |2-
            Handle data for all Ubisoft mobile games, create a homemade ETL scheduled with Airflow on AWS Cloud.

            Responsabilities includes:

            * Creatig a new Python framework to support a homemade ETL (migrating from individual scripts).
            * Migrating the base code from Python 2 to Python 3.
            * Promoting good practices and helped data analysts to create better SQL queries (Redshift).
            * Creating a data pipeline to gather Ads data (~20 partners), UA data (~15 partners), and user tracking (Python -> S3 -> Redshift).
            * Developing an optimized data flow to produce global KPIs for more than 15 games simultaneously (Airflow).
            * Studing different machine learning implementations (Sagemaker, AWS EMR/Spark, simple Python code) to understand their pros and cons.
            * Optimizing infrastructure costs (S3, EC2 sizing, Spot Instance).
            * Monitoring data quality by creating custom dashboards (Tableau).

        - title: Engine Programmer
          company: Ubisoft
          company_url: ''
          company_logo: org-ubisoft
          location: France
          date_start: '2015-01-01'
          date_end: '2016-01-01'
          description: |2-
            Assisted in the development of a new mobile engine by creating tools to monitor Lua VM memory, a homemade C++ package manager, and engine optimization.

            Responsabilities includes:

            * Implementing a new package manager using Gitlab & Premake.
            * Implementing a Lua memory tracker.

        - title: Gameplay Programmer
          company: Eugen Systems
          company_url: ''
          company_logo: org-eugensystems
          location: France
          date_start: '2012-01-01'
          date_end: '2015-01-01'
          description: |2-
            Implemente game systems, built a new pathfinding system and selection systems.

            Responsabilities includes:

            * Implementing new game systems (C++).
            * New pathfinding system (homemade, deterministic).
            * Fixing synchronization issues between players (from logs).

        - title: Backend Programmer
          company: Games-Fed
          company_url: ''
          location: France
          date_start: '2010-06-08'
          date_end: '2010-12-08'
          description: |2-
            Backend developer responsible for handling various types of events: Forza competition, meetings web application, ticketing web application, etc.
    design:
      columns: '1'

  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: All
          tag: '*'
        - name: Programming
          tag: Programming
        - name: AWS
          tag: AWS
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false

  - block: collection
    id: blog
    content:
      title: Blog
      subtitle: 'French only'
      text: ''
      # Choose how many pages you would like to display (0 = all pages)
      count: 1
      # Filter on criteria
      filters:
        folders:
          - post
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: compact
      columns: '2'

  - block: contact
    id: contact
    content:
      title: Contact Me
      subtitle:
      #text: |-
      #  Start leveraging your own data and empowering your whole team, contact me to build your very own data pipeline.
      # Contact (add or remove contact options as necessary)
      email: cedric.famin@gmail.com
      #appointment_url: 'https://calendly.com'
      # Automatically link email and phone or display as text?
      autolink: true
    design:
      columns: '2'
---
