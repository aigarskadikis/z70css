# Zabbix 7.0 CSS overrides

action=dashboard.view
```
/* "Data overview" widget. The line which reads from bottom to top, now we can read from left to right */
.list-table thead th .text-vertical {
    writing-mode: unset;
}
```

action=trigger.list&context=template
```
/* use all screen space for modual window */
.overlay-dialogue.modal-popup {
    top: unset;
    max-width: 98%;
}

/* cut margin to use more available pixels on screen */
.overlay-dialogue.modal {
    margin: 0;
}

/* increase length of trigger expression field. lower down height */
div.form-field textarea.monospace-font {
width: 80% !important;
field-sizing: normal;
height:2em;
}

/* increase length of trigger description field. lower down height */
div.form-field textarea#description {
width: 80% !important;
field-sizing: normal;
height:2em;
}

/* send bottom buttons from right to left */
.overlay-dialogue-footer {
    text-align: left;
}

/* give more screen space to popup screen */
div.modal-popup-large {
top:0;
}

/* hide operation data in the trigger list while browsing template */
.list-table thead tr th:nth-child(4),
.list-table tbody tr td:nth-child(4) {display:none}

/* hide tags column while browsing triggers at template level */
.list-table thead tr th:nth-child(7),
.list-table tbody tr td:nth-child(7) {display:none}

/* change border of input fields */
.multiselect, .z-select .focusable, z-select .focusable, .z-select .list,
z-select .list, input[type="text"], input[type="password"],
input[type="search"], input[type="number"], input[type="email"],
input[type="time"], input[type="file"], textarea, select {
    border-bottom: 1px solid #ddd;
    border-left: 1px solid #ddd;
    border-right: 1px solid #eee;
    border-top: 1px solid #eee;
}

```

action=map.view
```
/* increase font size in map */
.map-container {
font-size: 1.25em;
}
```

## "Data collecton" => "Hosts" 
action=host.list
```
/* hide web*/
.list-table thead tr th:nth-child(7),
.list-table tbody tr td:nth-child(7) {display:none}

/* hide Interfaces
.list-table thead tr th:nth-child(8),
.list-table tbody tr td:nth-child(8) {display:none}
*/

/* hide templates*/
.list-table thead tr th:nth-child(10),
.list-table tbody tr td:nth-child(10) {display:none}

/* hide encryption*/
.list-table thead tr th:nth-child(13),
.list-table tbody tr td:nth-child(13) {display:none}

/* hide tags*/
.list-table thead tr th:nth-child(15),
.list-table tbody tr td:nth-child(15) {display:none}
```

## "Data collecton" => "Hosts" => "Items"
action=item.list&context=host
```
/* hide tags in the items page at a host level */
.list-table thead tr th:nth-child(11),
.list-table tbody tr td:nth-child(11) {display:none}

/* hide origin lld rule */
table tbody tr td a.link-alt.orange {display:none}
table tbody tr td.wordbreak a.link-alt.orange {display:none}

/* hide origin template name */
table tbody tr td.wordbreak a.link-alt.grey {display:none}

/* do not let item Type to take 2 columns */
table thead tr th:nth-child(9), table tbody tr td:nth-child(9) {white-space:nowrap}

/* do not let item Name to take 2 columns */
table thead tr th:nth-child(3), table tbody tr td:nth-child(3) {white-space:nowrap}

/* do not let item Key to take 2 columns */
table thead tr th:nth-child(5), table tbody tr td:nth-child(5) {white-space:nowrap}

/* hide a reference to LLD rule */
table tbody tr td.wordbreak a.link-alt.teal.js-update-item {display:none}
```

## "Data collecton" => "Hosts" => "Triggers"
action=trigger.list&context=host&filter_hostids%5B0%5D=
```
/* hide operation data */
.list-table thead tr th:nth-child(5),.list-table tbody tr td:nth-child(5) {display:none}

/* hide tags at triggers page */
.list-table thead tr th:nth-child(9),
.list-table tbody tr td:nth-child(9) {display:none}

table tbody tr td a.link-alt.orange {display:none}

/* hide origin template name */
table tbody tr td a.link-alt.grey {display:none}

```

## special case when working under "Hosts" => "Triggers" and erasing the host object

action=trigger.list&context=host&filter_inherited=-1
```
/* a special case when filtering out multiple hosts */
/* hide operation data */
.list-table thead tr th:nth-child(6),
.list-table tbody tr td:nth-child(6) {display:none}

/* hide tags at triggers page */
.list-table thead tr th:nth-child(10),
.list-table tbody tr td:nth-child(10) {display:none}
```

