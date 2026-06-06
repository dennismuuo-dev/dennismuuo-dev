# Dennis Muuo

**Software Engineer** — <span id="typing"></span>

<p align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" alt="C" width="40" height="40"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/rust/rust-plain.svg" alt="Rust" width="40" height="40"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg" alt="Spring Boot" width="40" height="40"/>
</p>

<script>
const words = ["C", "Rust", "Spring Boot"];
let i = 0;
let j = 0;
let isDeleting = false;

function type() {
  const current = words[i];
  const display = document.getElementById("typing");
  
  if (isDeleting) {
    display.innerText = current.substring(0, j--);
  } else {
    display.innerText = current.substring(0, j++);
  }
  
  if (!isDeleting && j === current.length + 1) {
    isDeleting = true;
    setTimeout(type, 1500);
  } else if (isDeleting && j === 0) {
    isDeleting = false;
    i = (i + 1) % words.length;
    setTimeout(type, 500);
  } else {
    setTimeout(type, 100);
  }
}

type();
</script>
