<template>
    <div style="position: relative;">
    <section class="hero">
        <div class="content">
            <h1>Scale design & dev operations with Avocode Enterprise</h1>
            <p>
                A fully integrated suite of authentication & authorization products,
                Stytch’s platform removes the headache of.
            </p>
            <button class="theme-btn">Download The Theme Test</button>
        </div>
        <div class="chart">
            <img src="https://themewagon.github.io/pinwheel/images/banner-img.png" alt="Chart Image" />
        </div>

    </section>
        <!-- Image at the top right corner -->
        <img src="https://themewagon.github.io/pinwheel/images/banner-shape.svg" alt="Top Right Decoration"
            class="top-right-image" />
    </div>
</template>

<script>
</script>

<style scoped>
body {
    font-family: "Arial", sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f9f9f9;
}

/* Hero Section Styles */
.hero {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 50px 20px;
    font-family: Merriweather, sans-serif;
    color: white;
}

.content {
    max-width: 50%;
}

.content h1 {
    font-family: Merriweather, sans-serif;
    font-size: 55px;
    margin-bottom: 20px;
    color: black;
}

p {
    font-size: 16px;
    margin-bottom: 20px;
    color: grey;
}

.theme-btn {
    padding: 10px 20px;
    background-color: white;
    color: #020202;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    height: 50px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
}

.chart img {
    max-width: 600px;
    border-radius: 10px;
}

.top-right-image {
  position: absolute;
  top: -8rem;
  right: -1rem;
  width: 400px;
  z-index: -1;
}

/* Responsive Styles */
@media (max-width: 768px) {
    .hero {
        flex-direction: column;
        /* Stack the content and image vertically */
        align-items: center;
        text-align: center;
    }

    .content {
        max-width: 90%;
        /* Adjust the width of the content for smaller screens */
        text-align: left;
    }

    h1 {
        font-size: 32px;
        /* Reduce the font size for the heading */
    }

    p {
        font-size: 14px;
        /* Reduce the font size for the paragraph */
    }

    .chart img {
        max-width: 90%;
        /* Make the image responsive to the screen size */
        margin-top: 20px;
        /* Add spacing between the content and the image */
    }

    .theme-btn {
        width: 80%;
        /* Adjust button width for smaller screens */
        margin: 20px auto;
        /* Center the button */
    }
}

@media (max-width: 480px) {
    h1 {
        font-size: 24px;
        /* Further reduce the font size for very small screens */
    }

    p {
        font-size: 12px;
        /* Further reduce the paragraph font size */
    }

    .theme-btn {
        height: 40px;
        /* Adjust button height */
        font-size: 14px;
        /* Adjust button text size */
    }
}
</style>