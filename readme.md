# Styling rssLounge

I like [rssLounge](http://rsslounge.aditu.de/) a lot and
I think it's one of the best feed readers out there!
However, what I disliked from the beginning was the scrolling
behaviour of the header and the feed navigation,
so I made some changes to the style to get a more *Google Reader* like feeling.

![Modified rssLounge interface](https://raw.github.com/Akron/rssLounge-mod/master/rss-lounge-mod.jpg)

I deactivated the priority stuff completely - as I don't use it.
Overall it's not quite perfect - but works well for me.

The following code should be appended to `/public/stylesheets/all.css`
in rssLounge 1.7. It's tested with recent versions of Firefox and Chrome.

## Stylesheet extension
```css
/* Fix header*/
#feedsmenue,
  #header-left,
    #menue {
      position: fixed;
}

#filter {
  position: fixed;
  left: 260px;
  right: 70px;
  z-index: 10;
  margin-top: -50px;
}

#header-content {
  position: fixed;
  width: 100%;
  z-index: 5;
}

/* fix feed list*/
#feeds-list {
  position: fixed;
  width: 220px;
  margn-left: 10px;
  top: 82px;
  bottom: 32px;
  overflow-y: scroll;
  overflow-x: hidden;
}

/* Hide stats */
#stats {
  display: none;
}

/* feed list modifications */
#feeds-list h3 {
  max-height: 18px;
}

#feeds-list ul > li a.edit {
  left: 180px;
}

div#header {
 z-index: 2;
}

.ui-state-active {
  position: relative;
  z-index: 40;
}

/* Calendar modifications */
#calendar {
  position: relative;
  z-index: 20;
  margin-top: 24px;
  background-color: #F4F8F2;
}

/* Fix search field */
#feeds-list .search {
  padding: 5px 0px 5px 15px;
  position: fixed;
  width: 215px;
  bottom: 0px;
  left: 0;
  margin-left: 15px;
  border-radius: 6px 6px 0 0;
}

#feeds-list .search input {
  width:170px;
}

#feeds-list .search a {
  margin-left: -30px;
  top: 10px;
}

div.search {
  text-align: right;
  position: absolute;
  right: 0;
  margin-top: -10px;
}

/* Reposition progress bar */
div#progress {
  border: 2px solid #CCCCCC;
  border-radius: 6px 6px 6px 6px;
  background-color: #F4F8F2;
  margin: 5px;
  padding: 5px;
  bottom: 0;
  right: 0px;
  position: fixed;
  width: 120px;
}

/* Make add feed line wider */
#feedsmenue .add {
  width: 160px;
}

/* Modifications for small screens */
body.small #filter #actions {
  margin-top: 0;
}

body.small #filter #actions #unstarall {
  display: none;
}

body.small #filter {
  width: auto;
  left: 120px;
}

body.small #filter #filter-options {
  width: 150px;
  margin-left: -150px;
}

body.small #header h1 {
  background-position: left top;
  width: 85px;
}

body.small #filter-options a[id^="sort"],
  body.small select#view~a {
    display: none;
}
```

## Zebra Striping

![Modified rssLounge interface with zebra striping](https://raw.github.com/Akron/rssLounge-mod/master/rss-lounge-mod-2.jpg)

If you want to have zebra striping for unread entries,
you can additionally append the following rule:

```css
/* Zebra Striping */
#messages > li.unread:nth-of-type(even) {
  background-color: #ebe0c6
}
```

## Contributors

- **egrath** (zebra striping, bug report)