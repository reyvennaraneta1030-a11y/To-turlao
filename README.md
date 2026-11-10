
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Happy Birthday, Men!</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    min-height: 100vh;
    font-family: Georgia, serif;
    background: linear-gradient(135deg, #f7d9df, #f6e8d7);
    color: light blue;
    text-align: center;
    padding: 30px 15px;
}

h1 {
    color: #8d4358;
    font-size: 40px;
}

.intro {
    margin-bottom: 25px;
}

/* Hide checkbox */
#open-letter {
    display: none;
}

/* Envelope */
.envelope-wrap {
    width: 320px;
    height: 245px;
    position: relative;
    margin: 20px auto;
    perspective: 1000px;
}

.envelope {
    position: absolute;
    top: 55px;
    width: 100%;
    height: 180px;
    background: #c66b7d;
    border-radius: 10px;
    cursor: pointer;
    box-shadow: 0 12px 25px #70404b33;
}

.envelope::before {
    content: "";
    position: absolute;
    inset: 0;
    background: #d98796;
    clip-path: polygon(
        0 0, 50% 62%, 100% 0,
        100% 100%, 0 100%
    );
}

.flap {
    position: absolute;
    top: 0;
    width: 100%;
    height: 125px;
    background: #b9576d;
    clip-path: polygon(0 0, 100% 0, 50% 100%);
    transform-origin: top;
    transition: transform .8s;
    z-index: 4;
}

.seal {
    position: absolute;
    top: 100px;
    left: 50%;
    transform: translateX(-50%);
    width: 48px;
    height: 48px;
    background: #f8d8c9;
    color: #a34860;
    border-radius: 50%;
    display: grid;
    place-items: center;
    font-size: 25px;
    z-index: 5;
}

.tap-hint {
    position: absolute;
    top: 210px;
    width: 100%;
    font-size: 13px;
    font-weight: bold;
    cursor: pointer;
}

/* Birthday letter */
.letter {
    width: 90%;
    max-width: 650px;
    margin: auto;
    padding: 30px;
    background: #fffaf2;
    border-radius: 12px;
    box-shadow: 0 12px 30px #70404b22;
    text-align: left;
    line-height: 1.8;

    opacity: 0;
    max-height: 0;
    overflow: hidden;
    transform: translateY(30px);

    transition: all .9s ease;
}

.letter h2 {
    text-align: center;
    color: #a34f65;
}

.signature {
    text-align: right;
    margin-top: 25px;
}

/* Open animation */
#open-letter:checked ~ .envelope-wrap .flap {
    transform: rotateX(180deg);
}

#open-letter:checked ~ .envelope-wrap .seal {
    opacity: 0;
}

#open-letter:checked ~ .envelope-wrap .tap-hint {
    opacity: 0;
}

#open-letter:checked ~ .letter {
    opacity: 1;
    max-height: 1000px;
    transform: translateY(0);
    margin-top: 20px;
}

/* Pictures */
.photos {
    max-width: 900px;
    margin: 40px auto;
}

.photos h2 {
    color: #8d4358;
}

.gallery {
    display: grid;
    grid-template-columns:
        repeat(auto-fit, minmax(210px, 1fr));
    gap: 15px;
}

.gallery img {
    width: 100%;
    height: 280px;
    object-fit: cover;
    border: 7px solid #fffaf2;
    border-radius: 12px;
    box-shadow: 0 6px 16px #70404b25;
}

.footer {
    margin-top: 30px;
    color: #8d5965;
}

</style>
</head>

<body>

<h1>Happy Birthday, Men! 🎂</h1>

<p class="intro">
    I made a little something for you.
    Tap the letter to open it! 💌
</p>

<!-- Checkbox controls the letter -->
<input type="checkbox" id="open-letter">

<!-- ENVELOPE -->
<div class="envelope-wrap">

    <label class="envelope" for="open-letter">

        <span class="flap"></span>

        <span class="seal">♥</span>

    </label>

    <label class="tap-hint" for="open-letter">
        TAP THE LETTER TO OPEN
    </label>

</div>

<!-- BIRTHDAY MESSAGE -->
<div class="letter">

    <h2>Happy Birthday! ✨</h2>

    <p>Happy birthday, men!</p>

    <p>
        I hope your special day is filled with happiness,
        laughter, and unforgettable memories.
        Thank you for being you and for bringing good vibes
        and fun moments to the people around you.
    </p>

    <p>
        As you celebrate another year, I hope you keep
        chasing your dreams, learning new things, and
        enjoying every little moment along the way.
        May this year bring you more opportunities,
        success, good health, and plenty of reasons to smile.
    </p>

    <p>
        Always remember that you are appreciated.
        Keep being genuine, stay strong through every
        challenge, and never stop believing in yourself.
    </p>

    <p>
        Enjoy your day to the fullest.
        You deserve all the good things coming your way!
    </p>

    <p class="signature">
        Happy birthday once again!<br>
        — Your brother from another mother 💗
    </p>

</div>

<!-- PICTURE GALLERY -->
<section class="photos">

    <h2>Some Memories 📸</h2>

    <div class="gallery">

        <img src="1000013773.jpg"
             alt="Birthday memory 1">

        <img src="1000013772.jpg"
             alt="Birthday memory 2">

        <img src="1000013770.jpg"
             alt="Birthday memory 3">

    </div>

</section>



</body>
</html>

