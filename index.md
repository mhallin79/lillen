
<link href="styles/custom.css" rel="stylesheet" />

<div class="carousel">
  <div class="carousel-container">
    <!-- Images will be dynamically loaded here -->
  </div>
  <button class="prev" onclick="previousImage()">&#10094;</button>
  <button class="next" onclick="nextImage()">&#10095;</button>
</div>

<div class="photo-caption" id="photo-caption"></div>

<div class="thumbnails">
  <div class="thumbnail-scroll">
    <!-- Thumbnails will be dynamically loaded here -->
  </div>
</div>

# For Sale: 2016 Avan Ovation M5 C-Class Motorhome
## Sleeps 4, Low KM, One Owner, **Registered Until May 2026**

This one-owner, well-maintained 2016 Avan Ovation M5 C-Class motorhome has only 28,000 km and is fully equipped for comfort, adventure, and extended trips. **Registered until May 2026 with a normal car licence (no special licence required)**, it's road-ready for your next journey, offering a **very comfortable and easy-to-drive** experience.

**Price:** $120,000
**Location:** Woy Woy, NSW
**Mileage:** 28,000 km

### Key Features

* **Sleeps 4 comfortably** – Features a spacious electric drop-down bed for two adults and an additional bed over the cab.
* **Spacious lounge area** – Large windows, ample seating, and a drop-down bed for versatility and comfort.
* **Swivel front seats** – Maximise living space when parked, enhancing comfort.
* **Fully equipped kitchen** – 3-burner gas cooktop, gas oven with grill, microwave, and a 185L two-door 3-way fridge/freezer.
* **Private bathroom** – Separate shower and toilet for home-like convenience.
* **Entertainment system** – Integrated TV and stereo system.
* **Climate control** – Air conditioning and heating for year-round comfort in any weather.
* **Smooth driving experience** – Powered by a 3.0L Fiat Ducato turbo diesel engine, automatic 6-speed transmission, and cruise control.
* **Bullbar installed** – Extra protection for rural and off-road journeys.
* **Thule 2-bike carrier** – Conveniently bring bikes on your adventures.
* **Easy wind-out awning with festoon lights** – Create a cosy outdoor space.
* **Ambient lighting** – LED downlights and feature strip lighting for a warm atmosphere.
* **Off-grid capabilities** – Solar panels, water tanks, diesel heater, and a 125-litre diesel tank for extended trips.
* **Outdoor shower** – Hot and cold water for convenience after outdoor activities.
* **Additional features** – Reversing camera, GPS navigation, ample storage, and a full service history.

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
const imagesData = [
    { src: "images/lillen.jpg", alt: "Ready for its next adventure!" },
    { src: "images/window.jpg", alt: "Expansive rear window for stunning panoramic views" },
    { src: "images/festoon-lights.jpg", alt: "Awning with festoon lights for a warm, alfresco feel" },
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
    { src: "images/odometer.jpg", alt: "Odometer showing less than 28,000km, reflecting low mileage" }
];

function loadCarouselImages() {
    const carouselContainer = document.querySelector('.carousel-container');
    const thumbnailScroll = document.querySelector('.thumbnail-scroll');

    // Load carousel images
    imagesData.forEach((image, index) => {
        const imgElement = document.createElement('img');
        imgElement.src = image.src;
        imgElement.alt = image.alt;
        imgElement.style.display = index === 0 ? 'block' : 'none';

        const anchor = document.createElement('a');
        anchor.href = image.src;
        anchor.target = "_blank";
        anchor.appendChild(imgElement);
        carouselContainer.appendChild(anchor);

        // Create corresponding thumbnail
        const thumbnail = document.createElement('img');
        thumbnail.src = image.src;
        thumbnail.alt = image.alt;
        thumbnail.classList.add('thumbnail');
        thumbnail.addEventListener('click', () => showImage(index));
        thumbnailScroll.appendChild(thumbnail);
    });
}

function showImage(index) {
    const images = document.querySelectorAll('.carousel-container img');
    const thumbnails = document.querySelectorAll('.thumbnail');
    const caption = document.getElementById('photo-caption');

    images.forEach((img, i) => {
        img.style.display = i === index ? 'block' : 'none';
    });

    // Track and highlight active thumbnail
    thumbnails.forEach((thumb, i) => {
        thumb.classList.toggle('active', i === index);
        if (i === index) {
            // Scroll the active thumbnail into view
            thumb.scrollIntoView({ behavior: 'smooth', inline: 'center', block: 'nearest' });
        }
    });

    // Update the photo caption based on the active image alt text
    caption.textContent = imagesData[index].alt;

    currentIndex = index;
}


function nextImage() {
    currentIndex = (currentIndex + 1) % imagesData.length;
    showImage(currentIndex);
}

function previousImage() {
    currentIndex = (currentIndex - 1 + imagesData.length) % imagesData.length;
    showImage(currentIndex);
}

// Initialize
let currentIndex = 0;
document.addEventListener('DOMContentLoaded', () => {
    loadCarouselImages();
    showImage(0);
});


</script>
