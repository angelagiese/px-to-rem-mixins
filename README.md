<h1>px to rem mixins</h1>
<p>Just simple LESS and Sass mixins to convert pixel value font sizes and line heights to rem. This is something I use often as I recieve font sizes and line height as pixel values in design guidelines for projects I help out with.</p>

<h2>Usage</h2>
<p>The idea is to include these mixins into your project to make styling easier to match design guidelines.
Each mixin outputs:</p>
<ol>
<li>A pixel value as a backup for older browsers that don't understand rem</li>
<li>A rem value for the relative value</li>
</ol>

Simply install or download this repo to your local computer, then either:
<ul>
<li>Include the .less or .sass file in this repo into your own project OR</li>
<li>Copy and paste the contents of the .less or .sass files into your own .less or .sass files.</li>
</ul>

<h3>LESS usage</h3>
<p>Import into your .less file with <code>@import "px-to-rem";</code></p>
<p>x is the pixel size needed: <code>.font-size(x)</code> and <code>.line-height(x);</code></p>

<pre>
.some-element {
    .font-size(16);
    .line-height(32);
}
</pre>
<p>May output as:</p>
<pre>
.some-element {
    font-size: 16px; 
    font-size: 1rem;
    line-height: 32px; 
    line-height: 2rem;
}
</pre>

<h3>Sass usage</h3>
<p>Import into your .scss file with <code>@import "px-to-rem";</code></p>
<p>x is the pixel size needed: <code>@include font-size(x);</code> and <code>@include line-height(x);</code></p>

<pre>
.some-element {
    @include font-size(16);
    @include line-height(32);
}
</pre>
<p>May output as:</p>
<pre>
.some-element {
    font-size: 16px; 
    font-size: 1rem;
    line-height: 32px; 
    line-height: 2rem;
}
</pre>

<h2>Credit</h2>
<p>The idea from this came from an article on <a href="http://css-tricks.com/snippets/css/less-mixin-for-rem-font-sizing/">CSS-Tricks</a>. That article used mixins that used rem values, however. I needed to start with pixels then convert to rem.
<p>It would be great if you could keep credit to me in the files, plus spread the word about this repo. Thanks!</p>
