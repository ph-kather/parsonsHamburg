Mit diesen Aufgaben möchte ich die Grundlegende Syntax von funktionalen Elementen in Java einüben.
Hierbei geht es nur darum, die richtige Reihenfolge der Codeblöcke zu finden.
Zieht dafür einfach die Elemente aus dem Aufgabenbereich in den Lösungsbereich und prüft Eure Antwort.
Beachtet, dass meist nicht alle Elemente notwendig sind.

##  Aufgabe 1
Sortiert die Elemente so, dass alle Einträge der ursprünglichen Liste quadriert werden.

<div id="A1-sortableTrash" class="sortable-code"></div> 
<div id="A1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="A1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="A1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "List<Integer> neueListeMitZahlen = listeMitZahlen\n" +
    ".stream()\n" +
    ".map(z -> z * z)\n" +
    ".toList();\n" +
    ".iterate() #distractor\n" +
    ".map(z = z * z) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "A1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "A1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#A1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#A1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Aufgabe 2

Sortiert die Elemente so, dass alle Einträge entfernt werden, die größer oder gleich 100 sind.


<div id="A2-sortableTrash" class="sortable-code"></div> 
<div id="A2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="A2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="A2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "List&lt;Integer&gt; neueListeMitZahlen2 = listeMitZahlen\n" +
    "  .stream()\n" +
    "  .filter(z -&gt; z &lt; 100)\n" +
    "  .toList();\n" +
    ".filter(z -&gt; z + 100) #distractor\n" +
    ".filter(z -&gt; z &gt;= 100) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "A2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "A2-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#A2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#A2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Aufgabe 3
Sortiert die Elemente so, dass der Code alle Einträge kleiner oder gleich 0 entfernt, und anschlißend eine neue Liste erzeugt, der diese in ihren "Kehrwert" umwandelt (also z -> 1/z).


<div id="A3-sortableTrash" class="sortable-code"></div> 
<div id="A3-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="A3-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="A3-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "List<Double> neueListeMitZahlen3 = listeMitZahlen\n" +
    ".stream()\n" +
    ".filter(z -> z > 0)\n" +
    ".map(z ->  1.0 / z)\n" +
    ".toList();\n" +
    "  \n" +
    ".filter(z -> z <= 0) #distractor\n" +
    "List<Integer> neueListeMitZahlen2 = listeMitZahlen #distractor\n" +
    ".map(z ->  z != 0) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "A3-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "A3-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#A3-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#A3-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
