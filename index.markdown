Mit diesen Aufgaben möchte ich die Grundlegende Syntax von funktionalen Elementen in Java einüben.
Hierbei geht es nur darum, die richtige Reihenfolge der Codeblöcke zu finden.
Zieht dafür einfach die Elemente aus dem Aufgabenbereich in den Lösungsbereich und prüft Eure Antwort.
Beachtet, dass meist nicht alle Elemente notwendig sind.

##  Aufgabe 1
Sortiert die Elemente so, dass alle Einträge der ursprünglichen Liste quadriert werden

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
