---
# Leave the homepage title empty to use the site title
title:
date: 2026-01-01
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: About
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin

  - block: features
    id: research-areas
    content:
      title: Research Areas
      items:
        - name: High-Performance Computing
          description: Scalable algorithms, parallel numerical methods, performance optimization, and portability across modern HPC architectures.
          icon: server
          icon_pack: fas
        - name: Scientific Software
          description: Architecture, implementation, testing, and maintenance of production-scale computational physics and Earth-system model infrastructure.
          icon: code
          icon_pack: fas
        - name: Numerical Methods & Algorithms
          description: Dynamical cores, grid design, nesting, regridding, and transport schemes for multiscale geophysical simulation.
          icon: square-root-variable
          icon_pack: fas
        - name: Earth-System Modeling
          description: High-resolution atmosphere, ocean, land, and fully coupled climate modeling with SHiELD, MOM6, and LM4.
          icon: earth-americas
          icon_pack: fas

  - block: portfolio
    id: research
    content:
      title: Research
      subtitle: 'Earth-system modeling, dynamical cores, and coupled simulation. Click any project for details, figures and animations.'
      filters:
        folders:
          - research
        tags:
          - Dynamical Core
          - Coupled Modeling
    design:
      columns: '1'
      view: showcase
      flip_alt_rows: true

  - block: portfolio
    id: research-cfd
    content:
      title: Earlier Research &mdash; Computational Fluid Dynamics
      subtitle: 'Multiphase flow, turbulence, and sub-grid modeling: the numerical foundations behind the Earth-system work above.'
      filters:
        folders:
          - research
        tags:
          - Multiphase Flows
    design:
      columns: '1'
      view: showcase
      flip_alt_rows: true

  - block: collection
    id: featured
    content:
      title: Selected Publications
      filters:
        folders:
          - publication
        featured_only: true
      # Show all selected publications (0 = no limit)
      count: 0
      archive:
        enable: true
        text: View all publications
        # No `link:` override — the theme derives the archive URL from the
        # collection's own page, which stays correct under a subpath baseURL.
    design:
      columns: '2'
      view: card

  - block: markdown
    id: software
    content:
      title: Software & Models
      subtitle: 'Open-source scientific infrastructure I develop and contribute to at GFDL, spanning atmospheric dynamics, coupling, ocean, land, and sea-ice modeling.'
      text: |-
        <div class="software-grid">
          <a class="software-card" href="https://github.com/NOAA-GFDL/GFDL_atmos_cubed_sphere" target="_blank" rel="noopener">
            <span class="software-name">FV3</span>
            <span class="software-desc">The GFDL cubed-sphere finite-volume dynamical core. Grid nesting, the Duo-Grid, and transport schemes.</span>
          </a>
          <a class="software-card" href="https://github.com/NOAA-GFDL/SHiELD_build" target="_blank" rel="noopener">
            <span class="software-name">SHiELD</span>
            <span class="software-desc">GFDL's unified weather-to-climate modeling system built on FV3.</span>
          </a>
          <a class="software-card" href="https://github.com/NOAA-GFDL/FMS" target="_blank" rel="noopener">
            <span class="software-name">FMS</span>
            <span class="software-desc">The Flexible Modeling System coupler and exchange-grid infrastructure.</span>
          </a>
          <a class="software-card" href="https://github.com/NOAA-GFDL/MOM6" target="_blank" rel="noopener">
            <span class="software-name">MOM6</span>
            <span class="software-desc">Modular Ocean Model, coupled to SHiELD for high-resolution atmosphere-ocean simulation.</span>
          </a>
          <a class="software-card" href="https://github.com/NOAA-GFDL/LM4" target="_blank" rel="noopener">
            <span class="software-name">LM4</span>
            <span class="software-desc">GFDL land component, coupled to SHiELD for hydrological extremes.</span>
          </a>
          <a class="software-card" href="https://github.com/NOAA-GFDL/SIS2" target="_blank" rel="noopener">
            <span class="software-name">SIS2</span>
            <span class="software-desc">Sea Ice Simulator v2, the ice component of the coupled system.</span>
          </a>
        </div>
    design:
      columns: '1'

  - block: contact
    id: contact
    content:
      title: Contact
      subtitle: 'Interested in high-performance computing, numerical modeling, Earth-system simulation, or scientific software?'
      text: |-
        I am always glad to discuss research collaborations, scientific software
        development, and computational modeling.
      email: mouallem@princeton.edu
      contact_links:
        - icon: linkedin
          icon_pack: fab
          name: Joseph Mouallem
          link: 'https://www.linkedin.com/in/joseph-mouallem-614ab18b'
        - icon: graduation-cap
          icon_pack: fas
          name: Google Scholar
          link: 'https://scholar.google.com/citations?user=YcMMTB8AAAAJ&hl=en'
        - icon: github
          icon_pack: fab
          name: JosephMouallem
          link: 'https://github.com/JosephMouallem'
      # Automatically link email and phone or display as text?
      autolink: true
    design:
      columns: '2'
---
