// JavaScript file linked successfully
console.log("JavaScript is linked and working!");
document.addEventListener("DOMContentLoaded", function() {
    const items = document.querySelectorAll(".tech-item");

    function fadeInOnScroll() {
        items.forEach(item => {
            const rect = item.getBoundingClientRect();
            if (rect.top < window.innerHeight - 100) {
                item.style.opacity = 1;
                item.style.transform = "translateY(0)";
            }
        });
    }

    // Apply styles
    items.forEach(item => {
        item.style.opacity = 0;
        item.style.transform = "translateY(50px)";
        item.style.transition = "opacity 0.8s ease-out, transform 0.8s ease-out";
    });

    window.addEventListener("scroll", fadeInOnScroll);
    fadeInOnScroll(); // Trigger on load
});
