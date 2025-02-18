```{js}
document.addEventListener("DOMContentLoaded", function() {
  // Add event listeners to columns with data-bs-target
   document.querySelectorAll('.g-col-4').forEach(function(item) {
    item.addEventListener('click', function() {
      // Remove 'tool-active' class from all columns
      document.querySelectorAll('.g-col-4').forEach(col => col.classList.remove('tool-active'));
      
      // Add 'tool-active' class to the clicked column
      item.classList.add('tool-active');
      
      // Get the target collapse section
      const targetClass = item.getAttribute('data-show-target');

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

```{css}
div#tool-chooser>div.bg-light:hover {
  background-color: #cdcdcd !important; /* Darker shade on hover */
  transition: background-color 0.3s ease-in-out;
  cursor: pointer; /* Change cursor to indicate clickability */
}
div#tool-chooser .tool-active {
  background-color: #dfdfdf !important; /* Darker shade on select */
  border-color: #848484 !important;
}
```