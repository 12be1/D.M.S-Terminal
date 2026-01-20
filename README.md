<!DOCTYPE html>
<html>
<head>
  <title>United States Department of Metaphysical Science</title>
  <meta charset="utf-8">
</head>
<body>
  <h1>United States Department of Metaphysical Science</h1>

  <p>
    The United States Department of Metaphysical Science (D.M.S)
    operates under executive authority to research phenomena
    beyond conventional scientific frameworks.
  </p>

  <p>
    Certain materials associated with this department are restricted
    to authorized observers.
  </p>

  <hr>

  <small>
    © United States Government — Internal Use Only<br>
    Fictional agency. This site is part of a narrative project.
  </small>
</body>
</html>



<!DOCTYPE html>
<html>
<head>
  <title>D.M.S Secure Terminal</title>
  <meta charset="utf-8">
  <style>
    body {
      background: black;
      color: #00ff00;
      font-family: monospace;
      padding: 20px;
    }
    input {
      background: black;
      color: #00ff00;
      border: none;
      outline: none;
      font-family: monospace;
      width: 100%;
    }
  </style>
</head>
<body>

<pre id="output">
U.S. DEPARTMENT OF METAPHYSICAL SCIENCE
SECURE ACCESS TERMINAL v3.2

USERNAME:
</pre>

<input id="input" autofocus />

<script>
let stage = "username";
let username = "";

const output = document.getElementById("output");
const input = document.getElementById("input");

input.addEventListener("keydown", function(e) {
  if (e.key === "Enter") {
    const value = input.value.trim();
    input.value = "";

    if (stage === "username") {
      username = value;
      output.textContent += value + "\nPASSWORD:\n";
      stage = "password";
    }
    else if (stage === "password") {
      if (username === "observer" && value === "mirror") {
        output.textContent += "ACCESS GRANTED\n";
        output.textContent += "OBSERVER STATUS: PROVISIONAL\n\n";
        output.textContent += "Type 'help' for commands.\n";
        stage = "terminal";
      } else {
        output.textContent += "ACCESS DENIED\n";
        output.textContent += "SESSION TERMINATED\n";
        stage = "locked";
      }
    }
    else if (stage === "terminal") {
      handleCommand(value);
    }
  }
});

function handleCommand(cmd) {
  output.textContent += "> " + cmd + "\n";

  if (cmd === "help") {
    output.textContent +=
      "AVAILABLE COMMANDS:\n" +
      "help\n" +
      "ls\n" +
      "open log_01\n" +
      "status\n";
  }
  else if (cmd === "ls") {
    output.textContent +=
      "log_01\nlog_02\nlog_07\n";
  }
  else if (cmd === "open log_01") {
    output.textContent +=
      "LOG 01:\n" +
      "Subject enrolled voluntarily.\n" +
      "Reports awareness prior to observation.\n\n";
  }
  else if (cmd === "open log_07") {
    output.textContent +=
      "LOG 07:\n" +
      "Subject aware of observation.\n" +
      "Observation persists without equipment.\n" +
      "SEE: /observer/logs.html\n\n";
  }
  else if (cmd === "status") {
    output.textContent +=
      "OBSERVATION: ACTIVE\n" +
      "DISCONNECTION: NOT PERMITTED\n\n";
  }
  else {
    output.textContent += "UNKNOWN COMMAND\n";
  }
}
</script>

</body>
</html>






<!DOCTYPE html>
<html>
<head>
  <title>Observer Logs</title>
</head>
<body>
  <h2>OBSERVER ARCHIVE</h2>

  <p>
    If you are reading this, observation has already begun.
  </p>

  <p>
    Awareness does not require consent.
  </p>



