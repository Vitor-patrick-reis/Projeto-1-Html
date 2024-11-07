//Carosel de imagem 1

let currentSlide = 0;
const slides = document.querySelectorAll('.carousel-imagesteste img');
const totalSlides = slides.length;

function moveSlide(direction) {
    currentSlide += direction;

    if (currentSlide < 0) {
        currentSlide = totalSlides - 1;
    } else if (currentSlide >= totalSlides) {
        currentSlide = 0;
    }

    const offset = -currentSlide * 100;
    document.querySelector('.carousel-imagesteste').style.transform = `translateX(${offset}%)`;
}

 // Função para enviar o formulário
 function submitForm() {
    const name = document.getElementById("name").value;
    const email = document.getElementById("email").value;
    const message = document.getElementById("message").value;

    if (name && email && message) {
        // Simulação de envio do formulário
        document.getElementById("contactForm").reset();
        document.getElementById("formResponse").style.display = "block";
    } else {
        alert("Por favor, preencha todos os campos.");
    }
}

//Carrosel de imagem 2

function nextSlide(carouselId) {
    const carousel = document.getElementById(carouselId);
    const items = carousel.querySelectorAll('.carousel-item');
    let activeIndex = Array.from(items).findIndex(item => item.classList.contains('active'));

    items[activeIndex].classList.remove('active');
    activeIndex = (activeIndex + 1) % items.length;
    items[activeIndex].classList.add('active');
}

function prevSlide(carouselId) {
    const carousel = document.getElementById(carouselId);
    const items = carousel.querySelectorAll('.carousel-item');
    let activeIndex = Array.from(items).findIndex(item => item.classList.contains('active'));

    items[activeIndex].classList.remove('active');
    activeIndex = (activeIndex - 1 + items.length) % items.length;
    items[activeIndex].classList.add('active');
}

//Catalago

    const carousel = document.getElementById('carousel-ca');
    const navButtons = document.querySelectorAll('.carousel-nav-ca button');
    let currentIndex = 0;

    function updateCarousel() {
    carousel.style.transform = `translateX(-${currentIndex * 100}%)`;
    navButtons.forEach((button, index) => {
        button.classList.toggle('active', index === currentIndex);
    });
    }

    navButtons.forEach((button, index) => {
    button.addEventListener('click', () => {
        currentIndex = index;
        updateCarousel();
    });
    });

    // Responsividade automática (loop) - Opcional
    setInterval(() => {
    currentIndex = (currentIndex + 1) % navButtons.length;
    updateCarousel();
    }, 5000);

    //Mensagem automatica

    function showMessage() {
        const messageBox = document.getElementById('messageBox');
        messageBox.style.display = 'block';

        // Oculta a mensagem automaticamente após 10 segundos, se não for fechada
        setTimeout(() => {
            messageBox.style.display = 'none';
        }, 10000);
    }

    function closeMessage() {
        const messageBox = document.getElementById('messageBox');
        messageBox.style.display = 'none';
    }

    // Exibe a mensagem a cada 20 segundos
    setInterval(showMessage, 20000);
