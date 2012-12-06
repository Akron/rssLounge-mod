# Styling rssLounge

I like [rssLounge][http://rsslounge.aditu.de/] a lot and I think, it's one of the best feed readers out there.
However, what I disliked from the beginning was the scrolling behaviour of the header and the feed navigation, so I made some changes to the style to get a more *Google Reader* like feeling.

[[rss-lounge-mod.jpg]]

I deactivated the priority stuff completely, as I don't use it.
Overall it's not quite perfect - but works well for me.

The following code should be appended to */public/stylesheet/all.css*
in rssLounge 1.7. It's tested with recent versions of Firefox and Chrome.

## Stylesheet extension

```css
#feedsmenue,
  #header-left,
    #menue {
      position: fixed;
}

#filter {
  position:fixed;
  width:75%;
  z-index: 10;
  margin-top: -50px;
}

#header-content {
  position:fixed;
  width:100%;
  z-index:5;
}

#feeds-list {
  position: fixed;
  width: 220px;
  margn-left: 10px;
  top: 82px;
  bottom: 32px;
  overflow-y: scroll;
  overflow-x: hidden;
}

#stats {
  display: none;
}

#feeds-list ul li a.edit {
  left: 180px;
}

div#header {
  z-index: 2;
}

.ui-state-active {
  position: relative;
  z-index: 40;
}

#feeds-list h3 {
  max-height: 18px;
}

#calendar {
  position: relative;
  z-index: 20;
  margin-top: 24px;
  background-color: #F4F8F2;
}

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
```