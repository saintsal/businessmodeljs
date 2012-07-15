businessmodeljs
===============

Adds business model thumbnails to your html - automatically generated as inline SVG files on blockquotes. Based on Alex Osterwalders' Business Model Canvas.
http://www.businessmodelgeneration.com/canvas/

Requires jQuery. 


Instructions
------------
1. Include jQuery
2. Include bm.js
3. Create business models thumbnails around blockquotes by adding classes, .bm (or as you see fit) to denote a business model, then addition classes to select or highlight blocks.
* seg - customer segment
* val - value proposition
* res - key resource
* par - key partners
* act - key activitiess
* cha - channel
* rel - relationships
* cos - costs
* rev - revenues

You can also highlight the business model environment:

* ind - industry forces (good for highlighting competition and alternatives)
* mar - market forces (good for highlighting customer needs, jobs and problems)
* tre - trends
* mac - macro-economic forces (good for highlighting market size and investment issues)
(You can read up on the Business Model Environement in the book Business Model Generation, or here: http://www.businessmodelalchemist.com/2009/07/scanning-your-business-models.html )

Examples

```html
<blockquote class="bm">Business model</blockquote>
<blockquote class="bm res">Here's what we built. (Key resources selected.)</blockquote>
<blockquote class="bm cos-h res">How much will this actually cost to build to completion? (Key resources selected, costs highlighted.)</blockquote>
<blockquote class="bm seg">Let me tell you about this customer segment...</blockquote>
<blockquote class="bm seg mar">We've learned about their needs.</blockquote>
<blockquote class="bm seg ind">We learned about their alternatives.</blockquote>
<blockquote class="bm seg mac">And verified it's a growing market.</blockquote>
<blockquote class="bm mac">Our investors are eligible for tax credits.  </blockquote>
<blockquote class="bm res val-h seg">Will this segment use this asset this way?</blockquote>
<blockquote class="bm val seg">What do they really want?</blockquote>
<blockquote class="bm act-h val">Can we deliver what they want?</blockquote>
<blockquote class="bm act par-h">Can we get help supporting though a partner?</blockquote>
<blockquote class="bm cha tre">Domain experts have told us that customers are starting to trade expertise on forums.</blockquote>
<blockquote class="bm rev seg cha-h">Will customers buy subscriptions if we advertise on this forum?</blockquote>
<blockquote class="bm rev rel-h">Will this price affect retention?</blockquote>
```

4. Activate the thumbnails by calling this function. You probably want to do this in document.onReady(). (You can change the business model class to something other than .bm here. )
```javascript
    $('blockquote.bm').each(function(index) { jQuery(this).businessModel(); });
```
