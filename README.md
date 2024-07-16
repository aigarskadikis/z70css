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