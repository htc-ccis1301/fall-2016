---
title: "HTML Validation"
published: true
morea_id: asm-html-validate
morea_type: assessment
morea_sort_order: 1
morea_outcomes_assessed:
#  - out-basic-html
#  - out-html-validation
#  - out-github-basics
---

Validation Lab: Assessed ability to identify and correct HTML validation errors.

<link rel="stylesheet" href="https://cdn.oesmith.co.uk/morris-0.4.3.min.css">
<script src="//cdnjs.cloudflare.com/ajax/libs/raphael/2.1.0/raphael-min.js"></script>
<script src="https://cdn.oesmith.co.uk/morris-0.4.3.min.js"></script>

<div class="well">
  <div id="assessment" style="height: 250px;"></div>
</div>

<script>
Morris.Bar({
  element: 'assessment',
  hideHover: false,
  data: [
        { y: 'Very satisfactory (%)', num: 0 },
        { y: 'Satisfactory (%)', num: 0 },
        { y: 'Unsatisfactory (%)', num: 0 },
        { y: 'Absent (%)', num: 0 },
        ],
  xkey: 'y',
  ykeys: ['num'],
  resize: true,
  labels: ['Students']
});
</script>
