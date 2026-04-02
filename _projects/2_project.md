---
layout: page
title: Region IV-A Family Income and Expenditure Survey Data Viewer and Management System
description: CSCI 205 (Programming with Databases)
img: assets/img/cs205_header.jpg
importance: 2
category: acads
---

## **Overview**

`FIESViewer` is a Django-based web application designed to visualize, manage, and analyze household economic data from the Family Income and Expenditure Survey (FIES) for the CALABARZON Region in the Philippines. This region, located in Southern Luzon, is comprised of five provinces: Cavite, Laguna, Batangas, Rizal, and Quezon.

The application serves as a comprehensive tool for analyzing household economic data. It offers robust data visualization features, displaying income and expenditure patterns through interactive charts and statistics. For data management, it supports full CRUD (Create, Read, Update, Delete) operations for household records. Advanced filtering allows users to perform multi-criteria searches based on province, area type, income, and expenditure ranges. The application also provides provincial analysis, presenting aggregated statistics with weighted averages to deliver accurate regional insights. All of this is wrapped in a user-friendly interface, with intuitive navigation and responsive design, using the widely used Bootstrap CSS framework.

## **Data Source**

FIES is a nationwide survey that collects information on family income, sources of income, and household expenditure patterns in the Philippines. This is an open-access dataset provided by the Philippine Statistics Authority – Data Archive. Note that the FIES is conducted biennially, so its most recent iteration contains data from 2023. It has a total of 8 158 household entries with 19 data fields each.

## **Features**

The application implements nine views handling different functionalities, from homepage display to complex filtered queries and provincial statistics. Notably, some of the key view features include:

- Pagination: All list views use 20 items per page with Previous/Next navigation
- Form Validation: Comprehensive error handling with user-friendly messages
- Auto-calculation: New households have auto-incremented indices to avoid conflicts
- Weighted Statistics: Province view uses government-defined weighing factor for accurate population estimates
- Multi-criteria Filtering: Combines province, area type, income, and expenditure filters
- Success Messages: Django messages framework provides feedback on operations

## **Snapshots**

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cs205_fies1.png" title="Landing Page" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Landing page of the `FIESViewer` when opened using localhost. No deployment has been done due to time constraints. 
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cs205_fies2.png" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cs205_fies4.png" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cs205_fies5.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Some of the featured views of FIESViewer. From left to right: province information view, add new household form, search household querying tab. 
</div>

## **Tech Stack**

- Framework: Django 5.2.8
- Database: SQLite (development)
- Frontend Framework: Bootstrap 5.3.0
- Data Visualization: Chart.js
- Template Engine: Django Template Language
- Python Version: 3.14
- Additional Libraries: `django.contrib.humanize`
