<button id="toggleAll">Expandir/Contraer todo</button>

<details>
<summary>🐛 Errores</summary>
<p>Contenido de errores...</p>
</details>

<details>
<summary>📁 Rutas</summary>
<p>Contenido de rutas...</p>
</details>

<script>
document.getElementById('toggleAll').addEventListener('click', function() {
  let details = document.querySelectorAll('details');
  details.forEach(detail => {
    detail.open = !detail.open; // Cambia el estado de cada uno
  });
});
</script>
