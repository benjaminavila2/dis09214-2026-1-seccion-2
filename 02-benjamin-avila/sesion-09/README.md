# sesión 09 - 12/06

# Estados y Cámara Web — Introducción a la programación en p5.js

---

## ¿Cómo crear un sketch con estados diferentes?

La idea es manejar distintas "pantallas" (inicio, experiencia, final) dentro de un mismo sketch usando una variable de estado.

### Paso 1 — Crear y definir la variable de estado

Al principio del código (fuera de las funciones), se crea una variable que guarda en qué pantalla estamos. Empieza en `0`.

​```javascript
let estado = 0; // 0 = Inicio, 1 = Experiencia, 2 = Final
​```

### Paso 2 — Configurar el lienzo (`function setup`)

Se crea el lienzo de fondo donde va a ocurrir toda la "magia".

​```javascript
function setup() {
  createCanvas(400, 400);
  textAlign(CENTER, CENTER);
  textSize(24);
}
​```

### Paso 3 — Crear la estructura del estado (`function draw`)

Se usa un `switch`. Dependiendo del valor de la variable `estado`, el programa dibuja una cosa u otra.

​```javascript
function draw() {
  background(220);

  switch (estado) {
    case 0:
      pantallaInicio();
      break;
    case 1:
      pantallaExperiencia();
      break;
    case 2:
      pantallaFinal();
      break;
  }
}
​```

### Paso 4 — Programar visualmente cada estado (funciones propias)

Se crean las funciones definidas en el paso anterior. Cada una tiene un diseño y color distinto para notar el cambio.

​```javascript
function pantallaInicio() {
  background(135, 206, 250); // Azul claro
  fill(0);
  text("ESTADO 0: INICIO", width / 2, height / 2 - 20);
  textSize(16);
  text("Haz clic para continuar", width / 2, height / 2 + 20);
}

function pantallaExperiencia() {
  background(144, 238, 144); // Verde claro
  fill(0);
  textSize(24);
  text("ESTADO 1: JUEGO / EXPERIENCIA", width / 2, height / 2 - 20);

  // Aquí puedes poner elementos interactivos, por ejemplo un círculo que sigue al mouse
  fill(255, 100, 100);
  ellipse(mouseX, mouseY, 40, 40);

  fill(0);
  textSize(16);
  text("Haz clic para terminar", width / 2, height / 2 + 40);
}

function pantallaFinal() {
  background(255, 182, 193); // Rosado claro
  fill(0);
  textSize(24);
  text("ESTADO 2: FINAL", width / 2, height / 2 - 20);
  textSize(16);
  text("Haz clic para volver al inicio", width / 2, height / 2 + 20);
}
​```

### Paso 5 — La lógica del cambio y el reinicio

Para pasar de un estado a otro y volver al comienzo, se usa la función `mousePressed()`. Cada clic aumenta la variable. Si llega a 3 (después del estado 2), vuelve a 0.

​```javascript
function mousePressed() {
  // Avanzamos al siguiente estado
  estado = estado + 1;

  // Si pasamos del último estado (2), reiniciamos a 0
  if (estado > 2) {
    estado = 0;
  }
}
​```

📎 Ejemplo en p5.js: https://editor.p5js.org/PoliMujica/sketches/9vHePO158

---

## ¡Ojo! Hay muchas formas diferentes de cambiar de un estado a otro

### 1. Interacción con el teclado

**1.1. Por barra espaciadora o Enter:**

​```javascript
function keyPressed() {
  if (key === ' ' || keyCode === ENTER) { // ' ' es el espacio
    estado = estado + 1;
    if (estado > 2) estado = 0;
  }
}
​```

**1.2. Por teclas específicas (ej. números):** la tecla `1` lleva al inicio, la `2` a la experiencia y la `3` al final.

​```javascript
function keyPressed() {
  if (key === '1') estado = 0;
  if (key === '2') estado = 1;
  if (key === '3') estado = 2;
}
​```

📎
