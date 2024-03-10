
### setup
- appearance
  - theme: Shimmering focus
  - font: JetBrains Mono
- community plugins:
  - Style Settings
- Editor:
  - Readable line length: false
  - Show line number: true
  - vim key bindings: true

### hotkeys
- `ctrl + shift + p`: command palette
- `ctrl + p`: quick switcher: Open quick switcher

### css snippets

#### markgone

```css
body {
    --heading-size: inherit;
    --heading-line-height: 1em;  
    --list-indent-s: 1em;
    --font-weight-s: 400; }

/*- monospace font for source mode -*/
.markdown-source-view:not(.is-live-preview) {
    --font-text: 'JetBrains Mono', var(--font-monospace); }

/*- inline title -*/
.markdown-source-view:not(.is-live-preview) .inline-title {
    font-size: inherit;
    font-weight: var(--font-weight-s); }

/*- all headings: size -----------------------------------------------*/
.markdown-source-view:not(.is-live-preview) .HyperMD-header {
    font-size: var(--heading-size); }

/*- all headings: font weight -*/
.markdown-source-view:not(.is-live-preview) .HyperMD-header {
    font-weight: var(--font-weight-s); }

/*- all headings: line height -*/
.markdown-source-view:not(.is-live-preview) .HyperMD-header {
    line-height: var(--heading-line-height); }

/*- lists -----------------------------------------------*/
/* indents within lists */
.markdown-source-view:not(.is-live-preview) .cm-line.HyperMD-list-line {
    tab-size: var(--list-indent-s); }

/*- adjust ul-ol indents - don't use this, really. negative margins are BAD! -*/
/*.markdown-source-view:not(.is-live-preview) .cm-content > .cm-line.HyperMD-list-line {
    margin-left: -0.15em !important; }

/*- markdown elements -----------------------------------------------*/
.markdown-source-view:not(.is-live-preview) :is(.cm-formatting-header, .cm-formatting-list, .cm-formatting-list-ol, .cm-formatting-link, .cm-math) {
    color: var(--text-normal); 
    font-size: inherit; } 

/*- bold/italic/bold+italic font weight -*/
.markdown-source-view:not(.is-live-preview) :is(.cm-strong, .cm-em, .cm-em.cm-strong) {
    font-weight: var(--font-weight-s); }

/*- no italic style -*/
.markdown-source-view:not(.is-live-preview) :is(.cm-em, .cm-strong, .cm-em.cm-strong) {
    font-style: normal; }

/*- ==highlight== color -*/
.markdown-source-view:not(.is-live-preview) .cm-highlight {
    background-color: transparent; /* <rgb(211,211,211)> for a color */
    font-weight: var(--font-weight-s); }

/*- strikethrough -*/
.markdown-source-view:not(.is-live-preview) .cm-strikethrough {
    text-decoration: none; }

/*- internal links ----------------------------------------------*/
.markdown-source-view:not(.is-live-preview) :is(.cm-hmd-internal-link, .cm-hmd-internal-link:hover, .cm-hmd-barelink) {
    color: var(--text-normal);
    font-weight: var(--font-weight-s);
    text-decoration: none;  }

/*- external links ----------------------------------------------*/
.markdown-source-view:not(.is-live-preview) :is(.cm-link, .cm-link:hover, .cm-url, .cm-url:hover) {
    color: var(--text-normal);
    font-weight: var(--font-weight-s);
    text-decoration: none; }

/*- blockquotes ----------------------------------------------*/
.markdown-source-view:not(.is-live-preview) .cm-quote {
    color: var(--text-normal); }

/*- tags --------------------------------------------------------*/
.markdown-source-view:not(.is-live-preview) .cm-hashtag {
    color: var(--text-normal);
    font-size: inherit; }

.markdown-source-view:not(.is-live-preview) :is(.cm-hashtag.cm-hashtag-begin, .cm-hashtag.cm-hashtag-end) {
    background-color: inherit;
    padding-right: 0em;
    padding-left: 0em; }

/*- code --------------------------------------------------------*/
.markdown-source-view:not(.is-live-preview) .cm-inline-code {
    color: inherit;
    background-color: inherit;
    font-size: inherit;
    font-family: inherit; }

.markdown-source-view.mod-cm6:not(.is-live-preview) .cm-line.HyperMD-codeblock {
    padding-left: 0px;
    background-color: transparent;
    font-size: inherit;
    font-family: inherit; }

.markdown-source-view:not(.is-live-preview) .HyperMD-codeblock > * {
    color: var(--text-normal); }

/*- hide collapse icon ---------------------------------------------------------*/
.markdown-source-view:not(.is-live-preview) .cm-fold-indicator {
    display: none; }

/*- hide indentation guides ---------------------------------------------------------*/
.markdown-source-view:not(.is-live-preview) .cm-indent::before {
    display: none; }

```

#### vertical-line

```css
.cm-content {
  position: relative;
}

.mod-active .cm-content:after {
  position: absolute;
  content: "";
  top: 0;
  left: 111ex;
  bottom: 0;
  width: 8px;
  background-color: rgb(10 10 10 / 10%);
}

.theme-dark .mod-active .cm-content:after {
  background-color: rgb(245 245 245 / 10%);
}
```