<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Korkuteli Dijital Haber</title>
<!-- ... (stil ve head kısmı sizin verdiğiniz gibi) ... -->
<style>
  /* ... tüm CSS kodunuz burada ... */
</style>
</head>
<body>
<!-- ... tüm HTML gövdesi sizin verdiğiniz gibi ... -->
<script>
  // Hamburger Menü Toggle
  const hamburger = document.getElementById('hamburger');
  const navLinks = document.getElementById('nav-links');

  hamburger.addEventListener('click', () => {
    navLinks.classList.toggle('show');
  });

  // Slider otomatik hareket
  let currentSlide = 0;
  const slides = document.getElementById('slides');
  const totalSlides = slides.children.length;

  setInterval(() => {
    currentSlide = (currentSlide + 1) % totalSlides;
    slides.style.transform = `translateX(-${currentSlide * 100}%)`;
  }, 5000);

  // Basit iletişim formu işlemi (sayfa yenilemeden)
  document.getElementById('contact-form').addEventListener('submit', function(e) {
    e.preventDefault();
    alert('Mesajınız alındı, teşekkürler!');
    this.reset();
  });
</script>
</body>
</html>
