const scenes = {
  start: {
    text: "BIBI wakes up in a dreamy forest. Two paths lie ahead...",
    choices: [
      { text: "Follow the glowing butterflies 🦋", next: "butterflyPath" },
      { text: "Chase the mysterious melody 🎶", next: "melodyPath" }
    ]
  },
  butterflyPath: {
    text: "The butterflies lead her to a sparkling lake. A riddle appears: 'I’m always with you, even when far. What am I?'",
    choices: [
      { text: "Love ❤️", next: "correctAnswer" },
      { text: "Shadow 🌑", next: "wrongAnswer" }
    ]
  },
  melodyPath: {
    text: "The melody guides her to a tree with your initials carved. A note reads: 'To unlock the next step, say his nickname…'",
    choices: [
      { text: "BIBI 💘", next: "correctAnswer" },
      { text: "Cutiepie 🐣", next: "wrongAnswer" }
    ]
  },
  correctAnswer: {
    text: "<span class='shimmer'>✨ A portal opens! She steps through and finds a glowing message: 'You are my forever quest, BIBI. Love, your Biker 💌'</span>",
    choices: [
      { text: "Play again", next: "start" }
    ]
  },
  wrongAnswer: {
    text: "Oops! The forest giggles and resets. Try again, brave BIBI!",
    choices: [
      { text: "Back to start", next: "start" }
    ]
  }
};

function showScene(sceneKey) {
  const scene = scenes[sceneKey];
  const sceneDiv = document.getElementById("scene");
  sceneDiv.classList.remove("fade-in");
  void sceneDiv.offsetWidth; // Trigger reflow for animation
  sceneDiv.classList.add("fade-in");
  sceneDiv.innerHTML = scene.text;

  const choicesDiv = document.getElementById("choices");
  choicesDiv.innerHTML = "";
  scene.choices.forEach(choice => {
    const btn = document.createElement("button");
    btn.innerText = choice.text;
    btn.onclick = () => showScene(choice.next);
    choicesDiv.appendChild(btn);
  });
}

showScene("start");
