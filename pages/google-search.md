---
title: Google CSE
layout: page
permalink: /search/google.html
# optional Google search page, see docs/google.md
# set google-cse-id in _config.yml
---

## Google Site Search

<div class="alert alert-primary" role="alert">
  Bitte beachten Sie: CSE ist ein kostenloser Service von Google. Die Ergebnisse hängen von der Indexierung durch Dritte ab und können Werbung enthalten.
</div>

<script>
  (function() {
    var cx = '{{ site.google-cse-id }}';
    var gcse = document.createElement('script');
    gcse.type = 'text/javascript';
    gcse.async = true;
    gcse.src = 'https://cse.google.com/cse.js?cx=' + cx;
    var s = document.getElementsByTagName['script'](0);
    s.parentNode.insertBefore(gcse, s);
  })();
</script>
<gcse:search></gcse:search>
