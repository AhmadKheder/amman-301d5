

## display

Defines the element as a grid container and establishes a new grid formatting context for its contents.

Values:
+ grid – generates a block-level grid
+ inline-grid – generates an inline-level grid

```css
.container {
  display: grid | inline-grid;
}
```
Note: The ability to pass grid parameters down through nested elements (aka subgrids) has been moved to level 2 of the CSS Grid specification. Here’s a quick explanation.
# grid-template-columns
# grid-template-rows

Defines the columns and rows of the grid with a space-separated list of values. The values represent the track size, and the space between them represents the grid line.

Example :
```css
.container {
  grid-template-columns: 40px 50px auto 50px 40px;
  grid-template-rows: 25% 100px auto;
}
```
# Regex tutorial 
#### Regular expressions (regex or regexp) are extremely useful in extracting information from any text by searching for one or more matches of a specific search pattern (i.e. a specific sequence of ASCII or unicode characters).
#### Fields of application range from validation to parsing/replacing strings, passing through translating data to other formats and web scraping.
#### One of the most interesting features is that once youâ€™ve learned the syntax, you can actually use this tool in (almost) all programming languages â€‹â€‹(JavaScript, Java, VB, C #, C / C++, Python, Perl, Ruby, Delphi, R, Tcl, and many others) with the slightest distinctions about the support of the most advanced features and syntax versions supported by the engines).
#### Letâ€™s start by looking at some examples and explanations.



- display
#### Defines the element as a grid container and establishes a new grid formatting context for its contents.

* Values:

1. grid a generates a block-level grid
2. inline-grid
