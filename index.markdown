---
# Parsons Problems

Mit diesen Aufgaben möchte ich die Grundlegende Syntax von funktionalen Elementen in Java einüben.
Hierbei geht es nur darum, die richtige Reihenfolge der Codeblöcke zu finden.

Zieht dafür einfach die Elemente aus dem linken Bereich in den rechten Bereich und prüft Eure Antwort.
Gelegentlich kann die Einrückung problematisch sein.
Verschiebt daher alle Elemente nach ganz links außen.

---

##  Aufgabe 1
Sortiert die Elemente so, dass alle Einträge der ursprünglichen Liste quadriert werden

<div id="Aufgabe 1: Map-sortableTrash" class="sortable-code"></div> 
<div id="Aufgabe 1: Map-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Aufgabe 1: Map-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Aufgabe 1: Map-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "List&lt;Integer&gt; neueListeMitZahlen = listeMitZahlen\n" +
    ".stream()\n" +
    ".map(z -&gt; z * z)\n" +
    ".toList();\n" +
    ".map(z -&gt; z / 2) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Aufgabe 1: Map-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "Aufgabe 1: Map-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Aufgabe 1: Map-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Aufgabe 1: Map-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
