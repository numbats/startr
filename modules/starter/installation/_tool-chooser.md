```{js}
document.addEventListener("DOMContentLoaded", function() {
  // Add event listeners to columns with data-bs-target
   document.querySelectorAll('.g-col-4').forEach(function(item) {
    item.addEventListener('click', function() {
      // Get the target collapse section
      const targetClass = item.getAttribute('data-show-target');
      console.log(targetClass);

      // Collapse all other sections with .collapse class
      document.querySelectorAll('.collapse.instructions').forEach(function(collapse) {
        if (collapse.classList.contains(targetClass)) {
          new bootstrap.Collapse(collapse, { toggle: true })
        } else {
          new bootstrap.Collapse(collapse, { toggle: false }).hide();
        }
      });
    });
  });
});
```