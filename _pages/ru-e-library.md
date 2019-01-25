---
layout: page_full
language: ru
image: /assets/files/e-library.jpg
title: E-Library
permalink: /en/e-library
---
Э-Библиотека является нашим цифровым хранилищем промышленной и налоговой информации, ориентиров, информационных буклетов и многих других ресурсов, которые могут быть интересны Вам или Вашим клиентам.

Конфиденциальная информация, содержащаяся в хранилище, была тщательно исследована, разработана и все усилия были предприняты для обеспечения точности и своевременности данной информации. Тем не менее, прежде чем действовать, всегда лучше получить профессиональную консультацию.

Э-Библиотека постоянно обновляется и пополняется, поэтому мы настоятельно рекомендуем Вам почаще обращаться в данный раздел за новой информацией.

<table id="e-library" class="display dataTable" style="width:100%" role="grid">
    <thead>
        <tr>
            <th>Title</th>
            <th>Lang</th>
            <th>Type</th>
            <th>Month</th>
            <th>Year</th>
            <th>File</th>
        </tr>
    </thead>
    <tfoot>
        <tr>
            <th>Title</th>
            <th>Lang</th>
            <th>Type</th>
            <th>Month</th>
            <th>Year</th>
            <th>File</th>
        </tr>
    </tfoot>
    <tbody>
        {% for item in site.data.library.media %}
        <tr>
            <td>{{ item.title }}</td>
            <td>{{ item.language | upcase }}</td>
            <td>
                {{ item.types }}
            </td>
            <td>{{ item.date | date: "%b" }}</td>
            <td>{{ item.date | date: "%Y" }}</td>
            <td>
                <a href="{{ item.file }}" target="_blank">
                    <img src="/assets/images/download.png">
                </a>
            </td>
        </tr>
        {% endfor %}
    </tbody>
</table>
