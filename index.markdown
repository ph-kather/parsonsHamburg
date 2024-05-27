Mit diesen Aufgaben möchte ich die Grundlegende Syntax von funktionalen Elementen in Java einüben.
Hierbei geht es nur darum, die richtige Reihenfolge der Codeblöcke zu finden.
Zieht dafür einfach die Elemente aus dem Aufgabenbereich in den Lösungsbereich und prüft Eure Antwort.
Beachtet, dass meist nicht alle Elemente notwendig sind.

## Parsons 1 (Line Based Grader)
Re-arrange the blocks below so they print out "Hello World!"

<div id="p1-sortableTrash" class="sortable-code"></div>
<div id="p1-sortable" class="sortable-code"></div>
<div style="clear:both;"></div>
<p>
    <input id="p1-feedbackLink" value="Get Feedback" type="button" />
    <input id="p1-newInstanceLink" value="Reset Problem" type="button" />
</p>
<script type="text/javascript">
(function() {
  var initial = "print(\"Hello\")\n" +
    "print(\" \")\n" +
    "print(\"World\")\n" +
    "print(\"!\")";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "p1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "trashId": "p1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#p1-newInstanceLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.shuffleLines();
  });
  $("#p1-feedbackLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.getFeedback();
  });
})();
</script>


##  Aufgabe 1
Sortiert die Elemente so, dass alle Einträge der ursprünglichen Liste quadriert werden

<div id="Aufgabe1Map-sortableTrash" class="sortable-code"></div> 
<div id="Aufgabe1Map-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Aufgabe1Map-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Aufgabe1Map-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "List<Integer> neueListeMitZahlen = listeMitZahlen\n" +
    ".stream()\n" +
    ".map(z -> z * z)\n" +
    ".toList();\n" +
    ".map(z -> z / 2) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Aufgabe1Map-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "Aufgabe1:Map-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Aufgabe1Map-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Aufgabe1Map-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
