---
layout: page
permalink: /funding-case/
title: "The Case for Funding Mathematics"
description: "A draft, evidence-based case for funding mathematics: which skills bring value, to whom, and how each case fares with AI."
nav: false
---

This is part of an [AIRSHIP Lab](https://airship-lab.github.io/) program to understand mathematics and science in the age of AI, alongside AIRSHIP's larger study of the motivation and qualities of scientists at every stage of life and career. AIRSHIP Lab at UIC, where I am a founding core member, brings together researchers across disciplines to explore AI in science.

Why should anyone fund mathematics? This is a draft case built from evidence rather than advocacy. It asks which skills bring value to the mathematical profession and to others, what kind of value and for whom, and how each case fares as AI enters the work. It draws on the published accounts of mathematicians collected for the [Qualities of Mathematicians]({{ '/qualities/' | relative_url }}) study, a reading of those accounts for links between skills and the value they bring, and outside studies read in full.

Each argument shows its evidence, three strength ratings (what the accounts show, what outside studies show, and how well the claim as worded holds), its main caveat, and the evidence it still needs. Ratings and AI outlooks made by AI models are marked as judgments, not findings. See also [Mathematics in the Age of AI]({{ '/math-ai-age/' | relative_url }}). This is a draft for discussion. [Open it full screen]({{ '/assets/funding-case/index.html' | relative_url }}).

<iframe
  id="funding-case-frame"
  src="{{ '/assets/funding-case/index.html' | relative_url }}"
  width="100%"
  height="1600"
  style="border:0;display:block"
  title="The case for funding mathematics"
  loading="lazy"></iframe>

<script>
  // Fit the embedded page to its content and follow the site's light/dark setting (same-origin page).
  (function () {
    var frame = document.getElementById("funding-case-frame");
    function sync() {
      try {
        var doc = frame.contentDocument;
        if (!doc || !doc.documentElement) return;
        var theme = document.documentElement.getAttribute("data-theme");
        if (theme === "dark" || theme === "light") doc.documentElement.setAttribute("data-theme", theme);
        else doc.documentElement.removeAttribute("data-theme");
        frame.style.height = doc.documentElement.scrollHeight + 24 + "px";
      } catch (e) {}
    }
    frame.addEventListener("load", function () {
      sync();
      try {
        var doc = frame.contentDocument;
        if (window.ResizeObserver) new ResizeObserver(sync).observe(doc.body);
        doc.addEventListener("click", function () { setTimeout(sync, 60); });
        doc.defaultView.addEventListener("hashchange", function () { setTimeout(sync, 60); });
      } catch (e) {}
    });
    new MutationObserver(sync).observe(document.documentElement, { attributes: true, attributeFilter: ["data-theme"] });
  })();
</script>
