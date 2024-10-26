
<link href="styles/custom.css" rel="stylesheet" />

<div class="carousel">
  <div class="carousel-container">
    <!-- Images will be dynamically loaded here -->
  </div>
  <div class="photo-caption" id="photo-caption"></div> <!-- Caption under the feature image -->
  <button class="prev" onclick="previousImage()">&#10094;</button>
  <button class="next" onclick="nextImage()">&#10095;</button>
</div>

<div class="thumbnails">
  <div class="thumbnail-scroll">
    <!-- Thumbnails will be dynamically loaded here -->
  </div>
</div>


# For Sale: 2016 Avan Ovation M5 C-Class Motorhome
## Sleeps 4, Low KM, One Owner, Rego Until May 2025

This one-owner, well-maintained 2016 Avan Ovation M5 C-Class motorhome has only 28,000 km and is fully equipped for comfort, adventure, and extended trips. Registered until May 2025, it's road-ready for your next journey, offering a **very comfortable and easy-to-drive** experience.

**Price:** $139,990  
**Location:** Woy Woy, NSW  
**Mileage:** 28,000 km  

### Key Features

- **Sleeps 4 comfortably** – Features a spacious electric drop-down bed for two adults and an additional bed over the cab.
- **Spacious lounge area** – Large windows, ample seating, and a drop-down bed for versatility and comfort.
- **Swivel front seats** – Maximise living space when parked, enhancing comfort.
- **Fully equipped kitchen** – 3-burner gas cooktop, gas oven with grill, microwave, and a 185L two-door 3-way fridge/freezer.
- **Private bathroom** – Separate shower and toilet for home-like convenience.
- **Entertainment system** – Integrated TV and stereo system.
- **Climate control** – Air conditioning and heating for year-round comfort in any weather.
- **Smooth driving experience** – Powered by a 3.0L Fiat Ducato turbo diesel engine, automatic 6-speed transmission, and cruise control.
- **Bullbar installed** – Extra protection for rural and off-road journeys.
- **Thule 2-bike carrier** – Conveniently bring bikes on your adventures.
- **Easy wind-out awning with festoon lights** – Create a cosy outdoor space.
- **Ambient lighting** – LED downlights and feature strip lighting for a warm atmosphere.
- **Off-grid capabilities** – Solar panels, water tanks, diesel heater, and a 125-litre diesel tank for extended trips.
- **Outdoor shower** – Hot and cold water for convenience after outdoor activities.
- **Additional features** – Reversing camera, GPS navigation, ample storage, and a full service history.

Full list of **[features & specifications](specifications/index.md)**.

**Included Extras:** Camping chairs, table, annex mat.

**Bonus:** Comprehensive **[checklists and guides](guides/index.md)** to help the new owner make the most out of the van quickly.

### Layout

<a href="images/floorplan.png" target="_blank">
    <img src="images/floorplan.png" />
</a>

Make sure that you check out **[Caravan World's review](review/index.md)** of the Avan Ovation M5 from 2016.

Explore Australia’s hidden gems in comfort and style. With its one-owner history, low mileage, climate control, and registration valid until May 2025, it’s the perfect choice for your next adventure.

**Contact Mikael today on 0422 441 135 or [owner@lillen.au](mailto:owner@lillen.au) to arrange a viewing!**

{% include google-analytics.html %}

<script>
// JavaScript list of images
const images = [
    { src: "images/lillen.jpg", alt: "Ready for it's next adventure!" },
    { src: "images/window.jpg", alt: "Large panoramic rear window offering scenic views" },
    { src: "images/festoon-lights.jpg", alt: "Spacious awning with festoon lights, compatible with 12V & 240V" },
    { src: "images/left-side.jpg", alt: "Left side view of the motorhome exterior" },
    { src: "images/rear.jpg", alt: "Rear view with Thule bike racks attached" },
    { src: "images/entry.jpg", alt: "Entry door providing easy access to the interior" },
    { src: "images/drivers-seat.jpg", alt: "Comfortable driver's seat for long journeys" },
    { src: "images/front-table.jpg", alt: "Front table setup with swivel chairs, ideal for dining and relaxation" },
    { src: "images/front-table-travelling.jpg", alt: "Compact front table configuration while traveling" },
    { src: "images/kitchen.jpg", alt: "Fully equipped kitchen with modern amenities" },
    { src: "images/lounge-area.jpg", alt: "Comfortable lounge area with large windows for natural light" },
    { src: "images/bed.jpg", alt: "Spacious electric drop-down bed for two adults" },
    { src: "images/bunk-bed.jpg", alt: "Bunk bed over the cab for additional sleeping space" },
    { src: "images/bathroom.jpg", alt: "Well-designed bathroom with a separate shower stall" },
    { src: "images/shower.jpg", alt: "Private shower area with hot and cold water options" },
    { src: "images/odometer.jpg", alt: "Odometer showing less than 28,000 KM, reflecting low mileage" }
];

let currentIndex = 0;

// Function to create the carousel and thumbnails
function loadCarousel() {
    const carouselContainer = document.querySelector(".carousel-container");
    const thumbnailScroll = document.querySelector(".thumbnail-scroll");

    images.forEach((image, index) => {
        // Create main carousel images
        const anchor = document.createElement("a");
        anchor.href = image.src;
        anchor.target = "_blank";

        const img = document.createElement("img");
        img.src = image.src;
        img.alt = image.alt;

        anchor.appendChild(img);
        carouselContainer.appendChild(anchor);

        // Create thumbnails
        const thumb = document.createElement("img");
        thumb.src = image.src;
        thumb.alt = image.alt;
        thumb.classList.add("thumbnail");
        thumb.setAttribute("onclick", `showImage(${index})`);
        
        thumbnailScroll.appendChild(thumb);
    });

    // Show the first image and update caption
    showImage(0);
}

// Function to show specific image based on index
function showImage(index) {
    const carouselContainer = document.querySelector(".carousel-container");
    const images = carouselContainer.querySelectorAll("a");
    const caption = document.getElementById("photo-caption");

    images.forEach((image, i) => {
        image.style.display = i === index ? "block" : "none"; // Show the current image only
    });

    currentIndex = index;
    caption.textContent = images[index].querySelector("img").alt; // Update the footer caption
}

// Functions for navigating images
function previousImage() {
    const newIndex = (currentIndex - 1 + images.length) % images.length;
    showImage(newIndex);
}

function nextImage() {
    const newIndex = (currentIndex + 1) % images.length;
    showImage(newIndex);
}

// Initialize the carousel
document.addEventListener("DOMContentLoaded", loadCarousel);


</script>