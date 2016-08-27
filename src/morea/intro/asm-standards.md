---
title: "Internet technologies, standards, organizations, and architecture"
published: true
morea_id: asm-standards
morea_type: assessment
morea_sort_order: 1
morea_outcomes_assessed:
  - out-standards
  - out-web-arch
---

Quiz 1: Assessed knowledge of Internet technologies, standards, organizations, and architecture.

<link rel="stylesheet" href="https://cdn.oesmith.co.uk/morris-0.4.3.min.css">
<script src="//cdnjs.cloudflare.com/ajax/libs/raphael/2.1.0/raphael-min.js"></script>
<script src="https://cdn.oesmith.co.uk/morris-0.4.3.min.js"></script>

<div class="well">
  <div id="asm-standards" style="height: 250px;"></div>
</div>

<script>
Morris.Bar({
  element: 'asm-standards',
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
