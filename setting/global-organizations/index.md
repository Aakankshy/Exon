---
layout: page
title: Global Organizations
description: Master list of all global and local organizations
excerpt_separator: <!--more-->
---

## Foreword

Global organizations are often some of the most influential and powerful entities in Exon.

Unlike localized groups and organizations, global organizations often have a significant presence in most large nations all over the world.

This page includes a list of all of the global organizations in Exon (the following table) and a master list for every other organization (no matter the size) at the end.

<!--more-->

{% include table_of_contents.html %}

## Organization Master List

The following list consists of every organization in Exon that has been made so far; it dynamically updates as more organizations are made.

These organizations are also listed separately on the pages of their respective settings and areas of establishment.

<table style="text-align: center;">
  <colgroup>
    <col width="30%"/>
    <col width="70%"/>
  </colgroup>
  <thead>
    <tr class="header">
      <th>Page</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    {% assign url_ending = "organizations" %}
    {% for other in site.pages %}
      {% assign reversed_url = other.url | split: '/' | reverse %}
      {% if reversed_url[1] == url_ending %}
        <tr>
          <td class="table-of-contents-page-title">
            <a href="{{ site.baseurl }}{{ other.url }}">
              <strong>{{ other.title }}</strong>
            </a>
          </td>
          <td>{{ other.description }}</td>
        </tr>
      {% endif %}
    {% endfor %}
  </tbody>
</table>
