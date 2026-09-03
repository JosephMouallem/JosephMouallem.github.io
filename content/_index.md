---
# Leave the homepage title empty to use the site title
title:
date: 2026-01-01
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin

  # - block: features
  #   id: focus
  #   content:
  #     title: Focus Areas
  #     items:
  #       - name: Dynamical Core Development
  #         description: Numerical algorithms and CFD schemes in GFDL's FV3.
  #         icon: code
  #         icon_pack: fas
  #       - name: Grid Nesting
  #         description: Multiple same-level and telescoping nests.
  #         icon: layer-group
  #         icon_pack: fas
  #       - name: Duo-Grid
  #         description: Removing cubed-sphere grid imprinting.
  #         icon: border-all
  #         icon_pack: fas
  #       - name: Atmosphere-Ocean Coupling
  #         description: SHiELD-MOM6-SIS2 coupled modeling.
  #         icon: water
  #         icon_pack: fas
  #       - name: Reproducibility & Testing
  #         description: FV3 and SHiELD regression testing.
  #         icon: vials
  #         icon_pack: fas
  #       - name: High Performance Computing
  #         description: Scalable, massively parallel simulation.
  #         icon: server
  #         icon_pack: fas

  # - block: experience
  #   id: experience
  #   content:
  #     title: Professional Positions
  #     # Date format for experience
  #     #   Refer to https://wowchemy.com/docs/customization/#date-format
  #     date_format: Jan 2006
  #     items:
  #       - title: Computational Scientist
  #         company: GFDL / NOAA
  #         company_url: 'https://www.gfdl.noaa.gov/'
  #         company_logo: ''
  #         location: Princeton, NJ, USA
  #         date_start: '2020-01-01'
  #         date_end: ''
  #         description: |2-
  #             Member of the FV3 team. Work includes:

  #             * Development of the FV3 dynamical core
  #             * Multiple same-level and telescoping grid nesting
  #             * Duo-Grid implementation to eliminate grid imprinting
  #             * SHiELD-MOM6 coupled atmosphere-ocean model development
  #             * Reproducibility and regression testing for FV3 and SHiELD
  #       - title: Research Software Engineer
  #         company: Princeton University
  #         company_url: 'https://www.princeton.edu/'
  #         company_logo: ''
  #         location: Princeton, NJ, USA
  #         date_start: '2020-01-01'
  #         date_end: ''
  #         description: Research software engineering in support of atmospheric and ocean modeling at GFDL.
  #       - title: Postdoctoral Fellow and Sessional Lecturer
  #         company: University of Waterloo
  #         company_url: 'https://uwaterloo.ca/'
  #         company_logo: ''
  #         location: Waterloo, ON, Canada
  #         date_start: '2019-01-01'
  #         date_end: '2020-12-31'
  #         description: Direct Numerical Simulation of multiphase and turbulent compressible flows; teaching in mechanical engineering.
  #   design:
  #     columns: '2'

  - block: portfolio
    id: research
    content:
      title: Research
      subtitle: 'Click any project to see the details, figures and animations'
      # text: |-
      #   Click any project to see the details, figures and animations.
      filters:
        folders:
          - research
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      buttons:
        - name: All
          tag: '*'
        - name: Dynamical Core
          tag: Dynamical Core
        - name: Coupled Modeling
          tag: Coupled Modeling
        - name: CFD & Multiphase
          tag: Multiphase Flows
    design:
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: true

  - block: collection
    id: featured
    content:
      title: Featured Publications
      filters:
        folders:
          - publication
        featured_only: true
    design:
      columns: '2'
      view: card

  - block: collection
    id: publications
    content:
      title: Publications
      text: |-
        {{% callout note %}}
        Quickly discover relevant content by [filtering publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation

  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: |-
        Feel free to reach out!
      address:
        street: 201 Forrestal Road, Office 236
        city: Princeton
        region: NJ
        postcode: '08542'
        country: United States
        country_code: US
      email: mouallem@princeton.edu
      # contact_links:
      #   - icon: envelope
      #     icon_pack: fas
      #     name: joseph.mouallem@noaa.gov
      #     link: 'mailto:joseph.mouallem@noaa.gov'


        # - icon: graduation-cap
        #   icon_pack: fas
        #   name: Google Scholar
        #   link: 'https://scholar.google.com/citations?user=YcMMTB8AAAAJ&hl=en'
        # - icon: github
        #   icon_pack: fab
        #   name: GitHub
        #   link: 'https://github.com/JosephMouallem'
      # Automatically link email and phone or display as text?
      autolink: true
      # Email form provider
      form:
        provider: netlify
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: false
    design:
      columns: '2'
---
