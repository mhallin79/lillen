
<link href="styles/custom.css" rel="stylesheet" />

<div class="carousel">
  <div class="carousel-container">
      <a href="images/lillen.jpg" target="_blank">
          <img src="images/lillen.jpg" alt="Lillen" />
      </a>
      <a href="images/window.jpg" target="_blank">
          <img src="images/window.jpg" alt="Panoramic Window" />
      </a>
      <a href="images/festoon-lights.jpg" target="_blank">
          <img src="images/festoon-lights.jpg" alt="Festoon Lights" />
      </a>
      <a href="images/left-side.jpg" target="_blank">
          <img src="images/left-side.jpg" alt="External Left Side" />
      </a>
      <a href="images/rear.jpg" target="_blank">
          <img src="images/rear.jpg" alt="External Rear" />
      </a>
      <a href="images/drivers-seat.jpg" target="_blank">
          <img src="images/drivers-seat.jpg" alt="Drivers Seat" />
      </a>
      <a href="images/front-table.jpg" target="_blank">
          <img src="images/front-table.jpg" alt="Front Table" />
      </a>
      <a href="images/kitchen.jpg" target="_blank">
          <img src="images/kitchen.jpg" alt="Kitchen" />
      </a>
      <a href="images/lounge-area.jpg" target="_blank">
          <img src="images/lounge-area.jpg" alt="Lounge Area" />
      </a>
      <a href="images/bed.jpg" target="_blank">
          <img src="images/bed.jpg" alt="Bed" />
      </a>
      <a href="images/bunk-bed.jpg" target="_blank">
          <img src="images/bunk-bed.jpg" alt="Bunk Bed" />
      </a>
      <a href="images/odometer.jpg" target="_blank">
          <img src="images/odometer.jpg" alt="Odometer" />
      </a>
  </div>
  <button class="prev" onclick="previousImage()">&#10094;</button>
  <button class="next" onclick="nextImage()">&#10095;</button>
</div>

<div class="thumbnails">
  <div class="thumbnail-scroll">
      <img src="images/lillen.jpg" onclick="showImage(0)" alt="Lillen" class="thumbnail" />
      <img src="images/window.jpg" onclick="showImage(1)" alt="Panoramic Window" class="thumbnail" />
      <img src="images/festoon-lights.jpg" onclick="showImage(2)" alt="Festoon Lights" class="thumbnail" />
      <img src="images/left-side.jpg" onclick="showImage(3)" alt="External left side" class="thumbnail" />
      <img src="images/rear.jpg" onclick="showImage(4)" alt="External Rear" class="thumbnail" />
      <img src="images/drivers-seat.jpg" onclick="showImage(5)" alt="Drivers Seat" class="thumbnail" />
      <img src="images/front-table.jpg" onclick="showImage(6)" alt="Front Table" class="thumbnail" />
      <img src="images/kitchen.jpg" onclick="showImage(7)" alt="Kitchen" class="thumbnail" />
      <img src="images/lounge-area.jpg" onclick="showImage(8)" alt="Lounge Area" class="thumbnail" />
      <img src="images/bed.jpg" onclick="showImage(9)" alt="Bed" class="thumbnail" />
      <img src="images/bunk-bed.jpg" onclick="showImage(10)" alt="Bunk Bed" class="thumbnail" />
      <img src="images/odometer.jpg" onclick="showImage(11)" alt="Odometer" class="thumbnail" />
  </div>
</div>


# For Sale: 2016 Avan Ovation M5 C-Class Motorhome
## Sleeps 4, Low KM, One Owner, Rego Until May 2025

This one-owner, well-maintained 2016 Avan Ovation M5 C-Class motorhome has only 28,000 km and is fully equipped for comfort, adventure, and extended trips. Registered until May 2025, it's road-ready for your next journey, offering a **very comfortable and easy-to-drive** experience.

**Price:** $139,990 AUD  
**Location:** Woy Woy, NSW  
**Mileage:** 28,000 km  

### Key Features

- **Sleeps 4 comfortably** – Features a large electric drop-down bed that sleeps two adults and an additional bed over the cab for guests.
- **Great size lounge area** – Spacious seating with large windows and a large electric drop-down bed for extra comfort.
- **Swivel front seats for driver and passenger** – Maximises the living area when parked.
- **Fully equipped kitchen** – Includes a 3-burner gas cooktop, gas oven with grill, microwave, and a two-door 3-way 185L fridge (155L fridge and 30L freezer) for all your cooking needs.
- **Private bathroom** – Separate shower and toilet for added convenience.
- **Entertainment system** – TV and stereo for downtime during your trip.
- **Air conditioning** – Enjoy year-round comfort with efficient cooling in hot weather and reliable heating for colder days, ensuring a pleasant environment in all conditions.
- **Smooth driving experience** – Powered by a 3.0L Fiat Ducato turbo diesel engine with automatic 6-speed transmission and cruise control.
- **Bullbar installed** – Provides extra protection for rural or off-road journeys.
- **Thule 2-bike carrier** – Perfect for cyclists, making it easy to bring your bikes along.
- **Easy wind-out awning with festoon lights** – Creates a warm and inviting alfresco space for outdoor relaxation.
- **LED downlights and feature strip lighting** – Enhances the interior ambience.
- **Off-grid ready** – Equipped with solar panels, water tanks, a diesel heater, and a 125-litre diesel fuel tank for extended off-grid trips.
- **Additional features** – Reversing camera, GPS navigation, external shower, ample storage, and full service history.
- **Included extras** – Camping chairs, table, and annex mat for outdoor comfort.

### Floorplan

<a href="images/floorplan.jpg" target="_blank">
    <img src="images/floorplan.png" />
</a>

Make sure that you check out **[Caravan World's review](review/index.md)** of the Avan Ovation M5 from 2016.

I’ve also provided **[comprehensive checklists and guides](guides/index.md)** to help the new owner make the most out of the van quickly.

**Explore Austalia's hidden gems in comfort and style.** With its one-owner history, low mileage, air conditioning, and rego until May 2025, it’s the perfect choice for your next adventure.

Contact Mikael today on 0422 441 135 or [owner@lillen.au](mailto:owner@lillen.au) to arrange a viewing!

{% include google-analytics.html %}

<script>
  let currentIndex = 0;
  const images = document.querySelectorAll('.carousel img');
  const thumbnails = document.querySelectorAll('.thumbnail');

  function showImage(index) {
    currentIndex = index;
    images.forEach((img, i) => {
      img.style.display = (i === index) ? 'block' : 'none';
    });
    updateThumbnails();
  }

  function nextImage() {
    currentIndex = (currentIndex + 1) % images.length;
    showImage(currentIndex);
  }

  function previousImage() {
    currentIndex = (currentIndex - 1 + images.length) % images.length;
    showImage(currentIndex);
  }

  function updateThumbnails() {
    thumbnails.forEach((thumb, i) => {
      thumb.classList.toggle('active', i === currentIndex);
    });
  }

  thumbnails.forEach((thumb, index) => {
    thumb.addEventListener('click', () => showImage(index));
  });

  // Automatically show the first image
  showImage(currentIndex);
</script>