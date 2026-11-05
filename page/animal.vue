<style>
/* 原生 CSS：不依賴 Tailwind 或其他框架。 */
svg {
    vertical-align: middle
}

button {
    font-family: inherit
}

:root {
    --cream: #faf8f0;
    --ink: #3e4b3e;
    --green: #627c58;
    --muted: #767b6b;
    --line: #e5e5d9;
    --peach: #eaa586;
    --font-sans: Arial, 'Noto Sans TC', 'PingFang TC', 'Microsoft JhengHei', sans-serif
}

* {
    box-sizing: border-box
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 28px
}

body {
    margin: 0;
    background: var(--cream);
    color: var(--ink);
    font-family: var(--font-sans);
    -webkit-font-smoothing: antialiased
}

button,
a {
    -webkit-tap-highlight-color: transparent
}

button {
    font: inherit;
    cursor: pointer
}

a {
    color: inherit;
    text-decoration: none
}

button:focus-visible,
a:focus-visible {
    outline: 3px solid #d2936d;
    outline-offset: 5px
}

button svg,
a svg {
    flex-shrink: 0
}

button {
    touch-action: manipulation
}

.animal-home {
    max-width: 1440px;
    padding: 0 72px;
    margin: auto
}

.site-header {
    height: 104px;
    display: flex;
    align-items: center;
    border-bottom: 1px solid var(--line);
    gap: 36px
}

.brand {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 23px;
    font-weight: 800;
    letter-spacing: 1px
}

.brand-icon {
    display: grid;
    place-items: center;
    width: 42px;
    height: 42px;
    border-radius: 15px;
    background: #e5ebda;
    transform: rotate(-9deg);
    color: #627c58
}

.brand-small {
    font-size: 14px;
    margin-left: 5px;
    letter-spacing: 2px
}

.site-header nav {
    display: flex;
    gap: 30px;
    font-size: 13px;
    margin: auto
}

.site-header nav a {
    display: flex;
    align-items: center;
    gap: 7px;
    padding: 12px 0
}

.site-header nav a:hover {
    color: #b4795b
}

.header-tag {
    font-size: 11px;
    display: flex;
    align-items: center;
    gap: 7px;
    color: var(--muted);
    letter-spacing: 1px
}

.header-tag>span,
.scene-label>span {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: #8fa47a
}

.hero {
    display: grid;
    grid-template-columns: 1fr 1.1fr;
    align-items: center;
    gap: 40px;
    padding: 68px 0 57px;
    min-height: 610px
}

.eyebrow {
    font-size: 10px;
    letter-spacing: 2px;
    display: flex;
    align-items: center;
    gap: 8px;
    color: var(--muted);
    line-height: 1.8;
    font-weight: 500
}

.hero h1 {
    font-size: clamp(43px, 4.5vw, 63px);
    letter-spacing: 3px;
    font-weight: 800;
    line-height: 1.45;
    margin: 22px 0 23px
}

.hero h1>span {
    position: relative;
    white-space: nowrap;
    color: var(--green)
}

.hero h1 svg {
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 100%;
    height: 15px;
    fill: none;
    stroke: #e9bda2;
    stroke-width: 5;
    stroke-linecap: round;
    z-index: -1
}

.hero h1 i {
    font-style: normal;
    color: #d79977
}

.hero-copy>p {
    color: #757969;
    font-size: 14px;
    line-height: 2;
    letter-spacing: .7px;
    margin: 0 0 28px
}

.primary-button {
    border: 1px solid var(--green);
    background: var(--green);
    color: #fffef4;
    border-radius: 9px;
    padding: 15px 21px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 18px;
    font-size: 13px;
    letter-spacing: .6px;
    box-shadow: 0 4px 0 #465c4018;
    transition: transform .2s, background .2s
}

.primary-button:hover {
    background: #4d6744;
    transform: translateY(-2px)
}

.hero-footnote {
    font-size: 11px;
    color: #929584;
    display: flex;
    align-items: center;
    gap: 8px;
    margin-top: 20px
}

.hero-footnote>span {
    font-size: 20px;
    color: #c4ac7b
}

.hero-art {
    position: relative;
    height: 450px;
    width: 100%;
    isolation: isolate
}

.scene-sky {
    position: absolute;
    inset: 32px 0 22px;
    border-radius: 48% 48% 30% 30%;
    background: #e9eedf;
    overflow: hidden;
    border: 1px solid #e0e6d3
}

.hill {
    position: absolute;
    width: 130%;
    height: 170px;
    border-radius: 50%;
    bottom: -40px;
    left: -25%;
    background: #bdc9a6
}

.hill-front {
    left: 15%;
    bottom: -80px;
    background: #d0d8b9;
    height: 190px
}

.sun-doodle {
    position: absolute;
    right: 21%;
    top: 40px;
    color: #dbb069
}

.cloud {
    position: absolute;
    width: 58px;
    height: 16px;
    background: #faf9ec;
    border-radius: 30px;
    top: 72px;
    left: 20%;
    opacity: .9
}

.cloud:before {
    content: '';
    position: absolute;
    width: 27px;
    height: 27px;
    border-radius: 50%;
    background: inherit;
    bottom: 0;
    left: 14px
}

.cloud-two {
    top: 133px;
    left: 73%;
    transform: scale(.7)
}

.scene-label {
    position: absolute;
    top: 35px;
    left: 4%;
    background: #fffdf6;
    border: 1px solid #e0e2d2;
    padding: 10px 13px;
    display: flex;
    gap: 7px;
    align-items: center;
    font-size: 10px;
    letter-spacing: .8px;
    border-radius: 7px;
    transform: rotate(-7deg);
    z-index: 3
}

.animal-drawing {
    width: 100%;
    display: block;
    height: auto
}

.animal-in-scene {
    position: absolute;
    bottom: 56px;
    width: 43%;
    z-index: 2
}

.scene-bunny {
    left: 0;
    bottom: 78px;
    transform: rotate(-7deg)
}

.scene-capy {
    right: -1%;
    bottom: 72px;
    transform: rotate(6deg)
}

.scene-cat {
    left: 28%;
    bottom: 29px;
    width: 46%;
    z-index: 3
}

.flower {
    display: block;
    font-size: 47px;
    color: #f5e6b8;
    line-height: 1;
    text-shadow: 0 1px 0 #a8ac7f
}

.hero-art>.flower {
    position: absolute;
    z-index: 4
}

.flower-one {
    left: 5%;
    bottom: 50px;
    color: #fff4dc;
    transform: rotate(14deg)
}

.flower-two {
    right: 10%;
    bottom: 36px;
    font-size: 36px;
    color: #e5ac8e
}

.flower-three {
    right: 1%;
    top: 169px;
    font-size: 31px;
    color: #fff7d8
}

.grass {
    position: absolute;
    bottom: 81px;
    font-size: 47px;
    color: #8c9e77;
    z-index: 4
}

.grass-one {
    left: 19%;
    transform: rotate(-14deg)
}

.grass-two {
    right: 21%;
    bottom: 57px
}

.scene-note {
    position: absolute;
    bottom: -2px;
    left: 50%;
    transform: translateX(-50%) rotate(-4deg);
    white-space: nowrap;
    font-family: Georgia, serif;
    font-style: italic;
    font-size: 16px;
    color: #859274
}

.hello-bubble {
    position: absolute;
    top: 135px;
    left: 36%;
    border: 1px solid #dddccb;
    border-radius: 15px 15px 15px 0;
    padding: 10px 14px;
    font-size: 11px;
    background: #fffdf5;
    transform: rotate(4deg);
    z-index: 4
}

.divider-note {
    display: flex;
    align-items: center;
    gap: 22px;
    margin: 0 0 64px
}

.divider-note>span {
    height: 1px;
    background: var(--line);
    flex: 1
}

.divider-note p {
    display: flex;
    align-items: center;
    gap: 9px;
    font-size: 11px;
    letter-spacing: 1px;
    color: #8a907a
}

.section-heading {
    display: flex;
    align-items: end;
    justify-content: space-between;
    gap: 20px;
    margin-bottom: 27px
}

h2 {
    font-size: 25px;
    font-weight: 700;
    letter-spacing: 1px;
    margin: 9px 0 0;
    line-height: 1.5
}

.section-note {
    font-size: 11px;
    color: #8c907f;
    letter-spacing: .5px;
    display: flex;
    align-items: center;
    gap: 14px
}

.section-note>span {
    font-size: 30px;
    color: #b3b895
}

.friends-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 24px
}

.friend-card {
    min-width: 0;
    border: 1px solid #e4e4d7;
    border-radius: 17px;
    overflow: hidden;
    background: #fffdf7;
    box-shadow: 0 4px 0 #e6e4d830;
    transition: transform .2s
}

.friend-card:hover {
    transform: translateY(-4px)
}

.friend-portrait {
    position: relative;
    background: #f0e3cc;
    height: 254px;
    overflow: hidden
}

.friend-bunny .friend-portrait {
    background: #e9e8d8
}

.friend-capy .friend-portrait {
    background: #e5e9d9
}

.friend-portrait>.animal-drawing {
    height: 220px;
    width: 220px;
    position: absolute;
    bottom: -6px;
    left: 50%;
    transform: translateX(-50%)
}

.friend-number {
    position: absolute;
    left: 18px;
    top: 20px;
    font-size: 8px;
    letter-spacing: 1.5px;
    color: #8a8b73
}

.heart-button {
    position: absolute;
    right: 14px;
    top: 13px;
    z-index: 2;
    width: 37px;
    height: 37px;
    display: grid;
    place-items: center;
    border: 1px solid #fff6;
    border-radius: 50%;
    background: #fff9;
    color: #969781
}

.heart-button:hover,
.heart-button.liked {
    color: #c87c67;
    background: #fffbf2
}

.friend-portrait>.flower {
    position: absolute;
    left: 28px;
    top: 98px;
    font-size: 34px;
    color: #fffae9;
    transform: rotate(-13deg)
}

.portrait-tag {
    position: absolute;
    right: 12px;
    bottom: 14px;
    font-size: 10px;
    padding: 7px 10px;
    border: 1px solid #fff8;
    background: #fff9;
    border-radius: 20px;
    transform: rotate(-5deg);
    color: #747a5e
}

.friend-description {
    padding: 23px
}

.friend-name {
    display: flex;
    align-items: center;
    gap: 13px;
    flex-wrap: wrap
}

.friend-name h3 {
    font-size: 24px;
    letter-spacing: 2px;
    margin: 0;
    font-weight: 700
}

.friend-name>span {
    font-size: 8px;
    letter-spacing: 1.2px;
    color: #959581
}

.friend-description p {
    font-size: 12px;
    color: #818371;
    line-height: 1.9;
    margin: 12px 0 20px;
    min-height: 46px
}

.friend-link {
    font-size: 12px;
    font-weight: 600;
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-top: 1px dashed #e4e4d6;
    padding-top: 17px
}

.friend-link:hover {
    color: #b67c5c
}

.cozy-section {
    margin-top: 76px;
    display: grid;
    grid-template-columns: .9fr 1.1fr;
    gap: 56px;
    border: 1px solid #e2e5d7;
    background: #eef0e4;
    border-radius: 23px;
    padding: 43px 58px;
    align-items: center;
    position: relative;
    overflow: hidden
}

.cozy-illustration {
    position: relative;
    max-width: 320px;
    width: 100%;
    margin: auto;
    isolation: isolate
}

.cozy-illustration .animal-drawing {
    height: 275px
}

.cozy-floor {
    position: absolute;
    inset: 18% 0 0;
    border: 1px dashed #bec8a9;
    border-radius: 50%;
    z-index: -1
}

.cozy-sticker {
    position: absolute;
    left: -10px;
    top: 22px;
    background: #fffbed;
    padding: 9px 12px;
    transform: rotate(-10deg);
    font-size: 8px;
    letter-spacing: 1.5px;
    z-index: 1;
    box-shadow: 0 3px 6px #89936c0a
}

.pet-hearts {
    position: absolute;
    right: 0;
    top: 60px;
    color: #c1826d;
    font-size: 24px;
    transform: rotate(15deg)
}

.cozy-copy h2 {
    font-size: 28px;
    margin-top: 12px
}

.friend-tabs {
    display: flex;
    gap: 7px;
    margin: 19px 0
}

.friend-tabs button {
    padding: 8px 17px;
    border-radius: 20px;
    border: 1px solid #d6dcc8;
    background: transparent;
    color: #7d876c;
    font-size: 12px;
    min-height: 36px
}

.friend-tabs button.selected {
    background: #fffdf1;
    color: #4e6246;
    border-color: #abb897
}

.greeting {
    font-size: 13px;
    line-height: 1.9;
    min-height: 50px;
    color: #6d785f;
    margin: 0 0 16px
}

.pet-button {
    padding: 12px 17px;
    gap: 9px
}

.cozy-small {
    font-size: 10px;
    color: #89917c;
    margin: 14px 0 0
}

.daily-note {
    position: relative;
    margin-top: 36px;
    display: flex;
    align-items: center;
    gap: 35px;
    padding: 33px 35px;
    background: #f4eadb;
    border: 1px solid #e9decd;
    border-radius: 17px
}

.note-heading {
    flex-shrink: 0
}

.note-heading h2 {
    font-size: 17px;
    margin: 3px 0
}

.note-heading .eyebrow {
    font-size: 8px
}

.note-message {
    display: flex;
    align-items: center;
    gap: 10px;
    flex: 1
}

.note-message>span {
    font: 45px Georgia, serif;
    color: #b6aa8c;
    align-self: start;
    height: 28px
}

.note-message p {
    font-size: 13px;
    color: #7c725e;
    line-height: 1.8;
    letter-spacing: .5px;
    margin: 0
}

.note-button {
    border: none;
    background: transparent;
    display: flex;
    align-items: center;
    gap: 7px;
    font-size: 11px;
    color: #857b65;
    padding: 12px 0;
    white-space: nowrap;
    border-bottom: 1px solid #ccbea5
}

.note-button:hover {
    color: #9b6146
}

.daily-note>.flower {
    position: absolute;
    top: -16px;
    right: 21px;
    font-size: 32px;
    color: #f8d7a0
}

.closing {
    margin: 57px 0 42px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 25px;
    font-size: 11px;
    color: #969a86;
    letter-spacing: .8px
}

.closing>span {
    font-size: 15px;
    color: #b9be9d
}

footer {
    border-top: 1px solid var(--line);
    padding: 25px 0 29px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    color: #959984;
    font-size: 10px
}

.footer-brand {
    display: flex;
    align-items: center;
    gap: 7px;
    font-size: 13px;
    color: #768169
}

.footer-sign {
    font-size: 8px;
    letter-spacing: 1.4px;
    display: flex;
    align-items: center;
    gap: 7px
}

.footer-sign svg {
    color: #bf947a
}

.pet-animation {
    animation: bounce .5s ease-in-out
}

.animal-in-scene {
    animation: sway 6s ease-in-out infinite
}

.scene-bunny {
    animation-delay: -2s
}

.scene-capy {
    animation-delay: -4s
}

@keyframes sway {
    50% {
        translate: 0 -6px
    }
}

@keyframes bounce {
    40% {
        transform: translateY(-10px) rotate(-3deg)
    }

    70% {
        transform: translateY(-3px) rotate(3deg)
    }
}

@media(min-width:1441px) {
    .hero h1 {
        font-size: 65px
    }
}

@media(max-width:1100px) {
    .animal-home {
        padding: 0 40px
    }

    .header-tag {
        display: none
    }

    .site-header nav {
        margin: 0 0 0 auto
    }

    .hero {
        gap: 15px;
        min-height: 560px;
        padding: 40px 0 48px
    }

    .hero-art {
        height: 410px
    }

    .hero h1 {
        font-size: 49px
    }

    .friends-grid {
        gap: 16px
    }

    .friend-description {
        padding: 20px
    }

    .friend-name {
        gap: 8px
    }

    .friend-name>span {
        font-size: 7px
    }

    .cozy-section {
        padding: 35px;
        gap: 32px
    }

    .daily-note {
        gap: 22px;
        padding: 28px
    }

    .section-note {
        max-width: 170px;
        line-height: 1.8
    }
}

@media(max-width:800px) {
    .animal-home {
        padding: 0 26px
    }

    .site-header {
        height: 85px
    }

    .brand {
        font-size: 20px
    }

    .brand-small {
        font-size: 11px
    }

    .site-header nav {
        gap: 18px;
        font-size: 11px
    }

    .hero {
        grid-template-columns: 1fr 1fr;
        gap: 8px;
        min-height: 450px
    }

    .hero h1 {
        font-size: 39px;
        letter-spacing: 1px
    }

    .hero-copy>.eyebrow {
        font-size: 8px;
        letter-spacing: 1px
    }

    .hero-copy>p {
        font-size: 12px
    }

    .hero-art {
        height: 350px
    }

    .scene-sky {
        inset: 35px 0 30px
    }

    .scene-label {
        font-size: 8px;
        padding: 8px
    }

    .hello-bubble {
        top: 125px;
        font-size: 8px;
        padding: 8px;
        left: 28%
    }

    .scene-note {
        font-size: 12px
    }

    .sun-doodle {
        right: 15%;
        top: 30px;
        transform: scale(.8)
    }

    .cloud-one {
        left: 16%;
        top: 62px
    }

    .cloud-two {
        display: none
    }

    .scene-cat {
        bottom: 48px
    }

    .scene-bunny {
        bottom: 85px
    }

    .scene-capy {
        bottom: 79px
    }

    .flower-one {
        font-size: 34px
    }

    .divider-note {
        margin-bottom: 42px
    }

    .section-heading {
        align-items: start
    }

    .section-note {
        display: none
    }

    h2 {
        font-size: 23px
    }

    .friends-grid {
        gap: 13px
    }

    .friend-portrait {
        height: 211px
    }

    .friend-portrait>.animal-drawing {
        height: 180px;
        width: 180px
    }

    .friend-number {
        left: 12px;
        font-size: 7px;
        letter-spacing: .7px
    }

    .friend-portrait>.flower {
        left: 13px;
        top: 82px;
        font-size: 26px
    }

    .portrait-tag {
        right: 8px;
        font-size: 8px;
        bottom: 9px
    }

    .heart-button {
        width: 32px;
        height: 32px;
        right: 8px;
        top: 10px
    }

    .friend-description {
        padding: 16px
    }

    .friend-name {
        display: block
    }

    .friend-name h3 {
        font-size: 21px;
        margin-bottom: 3px
    }

    .friend-name>span {
        font-size: 7px
    }

    .friend-description p {
        font-size: 11px;
        min-height: 63px
    }

    .friend-link {
        font-size: 11px
    }

    .cozy-section {
        gap: 20px;
        padding: 28px;
        margin-top: 48px;
        grid-template-columns: 1fr 1.15fr
    }

    .cozy-copy h2 {
        font-size: 23px
    }

    .cozy-copy .eyebrow {
        font-size: 8px;
        letter-spacing: 1px
    }

    .cozy-illustration .animal-drawing {
        height: 235px
    }

    .cozy-sticker {
        font-size: 7px;
        left: -7px
    }

    .daily-note {
        flex-wrap: wrap;
        gap: 10px 23px;
        padding: 25px
    }

    .note-message {
        min-width: 220px
    }

    .note-button {
        margin-left: auto
    }

    .closing {
        font-size: 10px;
        gap: 14px
    }
}

@media(max-width:600px) {
    .animal-home {
        padding: 0 20px
    }

    .site-header {
        height: 77px;
        gap: 16px
    }

    .brand {
        font-size: 18px;
        gap: 7px;
        letter-spacing: .6px
    }

    .brand-icon {
        width: 34px;
        height: 34px;
        border-radius: 12px
    }

    .brand-small {
        font-size: 10px;
        display: block;
        margin: 0;
        letter-spacing: 3px
    }

    .site-header nav {
        gap: 16px;
        font-size: 10px
    }

    .site-header nav a:last-child svg {
        display: none
    }

    .hero {
        display: flex;
        flex-direction: column;
        padding: 39px 0 29px;
        gap: 6px;
        text-align: center
    }

    .hero-copy>.eyebrow {
        justify-content: center;
        letter-spacing: 1.4px;
        font-size: 8px
    }

    .hero h1 {
        font-size: 46px;
        line-height: 1.42;
        margin: 19px 0 20px;
        letter-spacing: 2px
    }

    .hero-copy>p {
        font-size: 12px;
        line-height: 1.9;
        margin-bottom: 23px
    }

    .primary-button {
        padding: 13px 20px;
        font-size: 12px
    }

    .hero-footnote {
        justify-content: center;
        margin-top: 14px;
        font-size: 10px
    }

    .hero-art {
        max-width: 390px;
        height: 335px;
        margin-top: 8px
    }

    .scene-sky {
        inset: 20px 5px 22px
    }

    .scene-label {
        left: 3%;
        top: 23px;
        font-size: 9px
    }

    .scene-bunny {
        bottom: 62px
    }

    .scene-capy {
        bottom: 61px
    }

    .scene-cat {
        bottom: 28px
    }

    .sun-doodle {
        right: 20%;
        top: 29px
    }

    .hello-bubble {
        top: 101px;
        left: 35%;
        font-size: 9px
    }

    .scene-note {
        bottom: 0;
        font-size: 14px
    }

    .flower-one {
        bottom: 32px;
        left: 5%
    }

    .flower-two {
        bottom: 28px
    }

    .flower-three {
        top: 124px
    }

    .grass-one {
        bottom: 54px
    }

    .grass-two {
        bottom: 37px
    }

    .divider-note {
        gap: 9px;
        margin: 13px 0 39px
    }

    .divider-note p {
        font-size: 9px;
        letter-spacing: 0;
        gap: 6px;
        white-space: nowrap
    }

    .divider-note p svg {
        width: 12px
    }

    .section-heading {
        margin-bottom: 21px
    }

    .eyebrow {
        font-size: 8px;
        letter-spacing: 1.5px
    }

    h2 {
        font-size: 22px;
        margin-top: 7px
    }

    .friends-grid {
        grid-template-columns: 1fr;
        gap: 22px
    }

    .friend-portrait {
        height: 259px
    }

    .friend-portrait>.animal-drawing {
        width: 232px;
        height: 242px;
        bottom: -14px
    }

    .friend-number {
        font-size: 8px;
        letter-spacing: 1.5px;
        left: 19px;
        top: 21px
    }

    .heart-button {
        width: 40px;
        height: 40px;
        top: 12px;
        right: 13px
    }

    .friend-portrait>.flower {
        font-size: 39px;
        left: 28px;
        top: 104px
    }

    .portrait-tag {
        font-size: 11px;
        bottom: 18px;
        right: 17px;
        padding: 8px 12px
    }

    .friend-description {
        padding: 22px
    }

    .friend-name {
        display: flex;
        gap: 14px
    }

    .friend-name h3 {
        font-size: 25px
    }

    .friend-name>span {
        font-size: 8px
    }

    .friend-description p {
        font-size: 12px;
        min-height: 0;
        line-height: 1.9;
        margin: 11px 0 18px
    }

    .friend-link {
        font-size: 12px;
        padding-top: 15px;
        min-height: 39px
    }

    .cozy-section {
        grid-template-columns: 1fr;
        padding: 28px 23px 32px;
        gap: 21px;
        margin-top: 42px;
        border-radius: 18px
    }

    .cozy-illustration {
        max-width: 250px
    }

    .cozy-illustration .animal-drawing {
        height: 235px
    }

    .cozy-sticker {
        left: -4px;
        top: 9px
    }

    .cozy-copy {
        text-align: center
    }

    .cozy-copy>.eyebrow {
        justify-content: center;
        font-size: 8px
    }

    .cozy-copy h2 {
        font-size: 25px
    }

    .friend-tabs {
        justify-content: center;
        margin: 16px 0
    }

    .friend-tabs button {
        min-height: 40px;
        padding: 9px 19px
    }

    .greeting {
        font-size: 12px;
        min-height: 46px
    }

    .cozy-small {
        font-size: 10px
    }

    .pet-button {
        min-height: 45px
    }

    .daily-note {
        display: block;
        text-align: center;
        padding: 29px 23px;
        margin-top: 24px
    }

    .note-heading .eyebrow {
        justify-content: center
    }

    .note-heading h2 {
        font-size: 19px;
        margin-top: 6px
    }

    .note-message {
        margin: 14px 0 11px;
        min-height: 65px;
        text-align: left;
        min-width: 0
    }

    .note-message p {
        font-size: 13px
    }

    .note-button {
        margin: auto;
        min-height: 44px
    }

    .closing {
        font-size: 10px;
        line-height: 1.8;
        gap: 10px;
        text-align: center;
        margin: 36px 0 30px
    }

    .closing>span {
        flex-shrink: 0
    }

    footer {
        flex-wrap: wrap;
        justify-content: center;
        text-align: center;
        padding: 25px 0;
        gap: 14px;
        font-size: 10px
    }

    .footer-brand {
        font-size: 12px
    }

    footer>span:nth-child(2) {
        width: 100%;
        order: 3
    }

    .footer-sign {
        font-size: 7px;
        letter-spacing: .8px
    }
}

@media(max-width:360px) {
    .animal-home {
        padding: 0 15px
    }

    .site-header nav {
        gap: 10px;
        font-size: 9px
    }

    .brand {
        font-size: 16px
    }

    .hero h1 {
        font-size: 41px
    }

    .hero-art {
        height: 301px
    }

    .hello-bubble {
        top: 87px;
        font-size: 8px
    }

    .scene-bunny {
        bottom: 61px
    }

    .scene-capy {
        bottom: 60px
    }

    h2 {
        font-size: 20px
    }

    .divider-note p {
        font-size: 8px
    }

    .hero-copy>.eyebrow {
        font-size: 7px
    }

    .friend-name>span {
        font-size: 7px
    }

    .friends-grid {
        gap: 19px
    }
}

@media(prefers-reduced-motion:reduce) {
    html {
        scroll-behavior: auto
    }

    *,
    *::before,
    *::after {
        animation: none !important;
        transition: none !important
    }
}
</style>
<template>
    <div v-if="isShow" class="animal-home">
        <header class="site-header"><a href="#" class="brand" aria-label="毛茸茸小日子首頁"><span class="brand-icon"><svg
                        xmlns="http://www.w3.org/2000/svg" width="23" height="23" viewBox="0 0 24 24" fill="none"
                        stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                        class="lucide lucide-paw-print" aria-hidden="true">
                        <circle cx="11" cy="4" r="2"></circle>
                        <circle cx="18" cy="8" r="2"></circle>
                        <circle cx="20" cy="16" r="2"></circle>
                        <path
                            d="M9 10a5 5 0 0 1 5 5v3.5a3.5 3.5 0 0 1-6.84 1.045Q6.52 17.48 4.46 16.84A3.5 3.5 0 0 1 5.5 10Z">
                        </path>
                    </svg></span><span>毛茸茸<span class="brand-small">小日子</span></span></a>
            <nav aria-label="主要導覽"><a href="#friends">認識小夥伴</a><a href="#cozy">療癒一下 <svg
                        xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none"
                        stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                        class="lucide lucide-heart" aria-hidden="true">
                        <path
                            d="M2 9.5a5.5 5.5 0 0 1 9.591-3.676.56.56 0 0 0 .818 0A5.49 5.49 0 0 1 22 9.5c0 2.29-1.5 4-3 5.5l-5.492 5.313a2 2 0 0 1-3 .019L5 15c-1.5-1.5-3-3.2-3-5.5">
                        </path>
                    </svg></a>
            </nav><span class="header-tag"><span></span> 今天也要可可愛愛</span>
        </header>
        <main>
            <section class="hero" aria-labelledby="hero-title">
                <div class="hero-copy">
                    <div class="eyebrow"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                            viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"
                            stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-sun" aria-hidden="true">
                            <circle cx="12" cy="12" r="4"></circle>
                            <path d="M12 2v2"></path>
                            <path d="M12 20v2"></path>
                            <path d="m4.93 4.93 1.41 1.41"></path>
                            <path d="m17.66 17.66 1.41 1.41"></path>
                            <path d="M2 12h2"></path>
                            <path d="M20 12h2"></path>
                            <path d="m6.34 17.66-1.41 1.41"></path>
                            <path d="m19.07 4.93-1.41 1.41"></path>
                        </svg> A LITTLE PAUSE, A LITTLE PAWS.
                    </div>
                    <h1 id="hero-title">把日子過得<br /><span>毛茸茸的<svg viewBox="0 0 360 16" preserveAspectRatio="none"
                                aria-hidden="true">
                                <path d="M3 10 Q170 1 355 9"></path>
                            </svg></span><i>。</i>
                    </h1>
                    <p>歡迎來到小動物的慢生活。<br />在這裡，把忙碌暫停，讓可愛陪你充充電。
                    </p><a class="primary-button" href="#friends">遇見你的小夥伴 <svg xmlns="http://www.w3.org/2000/svg"
                            width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor"
                            stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                            class="lucide lucide-arrow-down" aria-hidden="true">
                            <path d="M12 5v14"></path>
                            <path d="m19 12-7 7-7-7"></path>
                        </svg></a>
                    <div class="hero-footnote"><span>✳</span> 不用趕路，坐一下也很好。
                    </div>
                </div>
                <div class="hero-art" role="img" aria-label="奶油貓、糯米兔與阿慢水豚在花草間一起曬太陽">
                    <div class="scene-sky"><span class="sun-doodle"><svg xmlns="http://www.w3.org/2000/svg" width="67"
                                height="67" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.2"
                                stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-sun"
                                aria-hidden="true">
                                <circle cx="12" cy="12" r="4"></circle>
                                <path d="M12 2v2"></path>
                                <path d="M12 20v2"></path>
                                <path d="m4.93 4.93 1.41 1.41"></path>
                                <path d="m17.66 17.66 1.41 1.41"></path>
                                <path d="M2 12h2"></path>
                                <path d="M20 12h2"></path>
                                <path d="m6.34 17.66-1.41 1.41"></path>
                                <path d="m19.07 4.93-1.41 1.41"></path>
                            </svg></span><span class="cloud cloud-one"></span><span class="cloud cloud-two"></span><span
                            class="hill hill-back"></span><span class="hill hill-front"></span>
                    </div>
                    <div class="scene-label"><span></span> 慢慢村 · 晴時多可愛
                    </div>
                    <div class="animal-in-scene scene-bunny"><svg viewBox="0 0 240 250" fill="none" aria-hidden="true"
                            class="animal-drawing ">
                            <ellipse cx="120" cy="226" rx="78" ry="12" fill="#404d3820"></ellipse>
                            <path
                                d="M65 174 Q61 126 120 126 Q179 126 176 181 L177 211 Q174 228 153 225 L87 225 Q62 226 65 206Z"
                                fill="#fff9ec" stroke="#ded6c2" stroke-width="2"></path>
                            <ellipse cx="120" cy="188" rx="31" ry="33" fill="#fff2d9"></ellipse>
                            <ellipse cx="91" cy="64" rx="19" ry="51" transform="rotate(-12 91 64)" fill="#fff9ec"
                                stroke="#ded6c2" stroke-width="2"></ellipse>
                            <ellipse cx="148" cy="60" rx="18" ry="50" transform="rotate(10 148 60)" fill="#fff9ec"
                                stroke="#ded6c2" stroke-width="2"></ellipse>
                            <ellipse cx="91" cy="61" rx="8" ry="33" transform="rotate(-12 91 61)" fill="#ecc1b3">
                            </ellipse>
                            <ellipse cx="148" cy="59" rx="7" ry="32" transform="rotate(10 148 59)" fill="#ecc1b3">
                            </ellipse>
                            <path d="M52 112 Q52 68 119 68 Q186 68 187 112 L190 127 Q190 165 121 167 Q49 165 49 126Z"
                                fill="#fff9ec" stroke="#ded6c2" stroke-width="2"></path>
                            <ellipse cx="81" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                            <ellipse cx="159" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                            <ellipse cx="94" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
                            <ellipse cx="148" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
                            <path d="M116 132 Q120 129 124 132 L120 136Z" fill="#a16e61"></path>
                            <path d="M120 136 Q120 145 113 141 M120 136 Q120 145 127 141" stroke="#816754"
                                stroke-width="2" stroke-linecap="round"></path>
                            <path d="M79 183 L84 202 M162 183 L157 202" stroke="#ded6c2" stroke-width="3"
                                stroke-linecap="round"></path>
                            <path d="M103 188 L126 218 L135 183Z" fill="#ed9a5c"></path>
                            <path d="M124 184 L114 171 M128 184 L135 170" stroke="#82945b" stroke-width="6"
                                stroke-linecap="round"></path>
                            <path d="M82 217 L100 217 M143 217 L160 217" stroke="#ded6c2" stroke-width="3"
                                stroke-linecap="round"></path>
                        </svg>
                    </div>
                    <div class="animal-in-scene scene-capy"><svg viewBox="0 0 240 250" fill="none" aria-hidden="true"
                            class="animal-drawing ">
                            <ellipse cx="120" cy="226" rx="78" ry="12" fill="#404d3820"></ellipse>
                            <path
                                d="M65 174 Q61 126 120 126 Q179 126 176 181 L177 211 Q174 228 153 225 L87 225 Q62 226 65 206Z"
                                fill="#bc936e" stroke="#a97d58" stroke-width="2"></path>
                            <ellipse cx="120" cy="188" rx="31" ry="33" fill="#d5b18c"></ellipse>
                            <circle cx="76" cy="76" r="18" fill="#bc936e" stroke="#a97d58" stroke-width="2"></circle>
                            <circle cx="158" cy="76" r="18" fill="#bc936e" stroke="#a97d58" stroke-width="2"></circle>
                            <circle cx="76" cy="77" r="8" fill="#9b7558"></circle>
                            <circle cx="158" cy="77" r="8" fill="#9b7558"></circle>
                            <path
                                d="M52 113 Q53 76 97 76 L143 76 Q184 76 187 119 L191 137 Q192 164 158 168 L88 168 Q49 165 49 140Z"
                                fill="#bc936e" stroke="#a97d58" stroke-width="2"></path>
                            <ellipse cx="81" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                            <ellipse cx="159" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                            <ellipse cx="94" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
                            <ellipse cx="148" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
                            <ellipse cx="120" cy="141" rx="19" ry="12" fill="#d1ab85"></ellipse>
                            <path d="M114 137 L114 140 M126 137 L126 140 M112 148 Q120 151 128 148" stroke="#70513c"
                                stroke-width="2" stroke-linecap="round"></path>
                            <path d="M79 183 L84 202 M162 183 L157 202" stroke="#a97d58" stroke-width="3"
                                stroke-linecap="round"></path>
                            <circle cx="120" cy="65" r="16" fill="#efad4c"></circle>
                            <path d="M119 49 Q128 35 136 44 Q130 52 119 49" fill="#728650"></path>
                            <path d="M82 217 L100 217 M143 217 L160 217" stroke="#a97d58" stroke-width="3"
                                stroke-linecap="round"></path>
                        </svg>
                    </div>
                    <div class="animal-in-scene scene-cat"><svg viewBox="0 0 240 250" fill="none" aria-hidden="true"
                            class="animal-drawing is-happy">
                            <ellipse cx="120" cy="226" rx="78" ry="12" fill="#404d3820"></ellipse>
                            <path d="M176 193 C228 208 224 160 209 160" stroke="#efb780" stroke-width="22"
                                stroke-linecap="round"></path>
                            <path
                                d="M65 174 Q61 126 120 126 Q179 126 176 181 L177 211 Q174 228 153 225 L87 225 Q62 226 65 206Z"
                                fill="#efb780" stroke="#ce9667" stroke-width="2"></path>
                            <ellipse cx="120" cy="188" rx="31" ry="33" fill="#fff2d9"></ellipse>
                            <path d="M62 108 L59 46 Q59 37 69 44 L104 75 M138 73 L174 43 Q183 37 182 52 L178 111"
                                fill="#efb780" stroke="#ce9667" stroke-width="2"></path>
                            <path d="M70 82 L70 57 L90 78 M153 77 L173 55 L171 83" fill="#e69b8c"></path>
                            <path d="M52 112 Q52 68 119 68 Q186 68 187 112 L190 127 Q190 165 121 167 Q49 165 49 126Z"
                                fill="#efb780" stroke="#ce9667" stroke-width="2"></path>
                            <path d="M109 73 L111 87 M128 71 L127 87 M145 76 L140 88" stroke="#d39763" stroke-width="5"
                                stroke-linecap="round"></path>
                            <path d="M55 124 L39 120 M56 134 L40 136 M182 124 L200 120 M182 134 L198 136"
                                stroke="#ce9667" stroke-width="2" stroke-linecap="round"></path>
                            <ellipse cx="81" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                            <ellipse cx="159" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                            <path d="M88 121 Q94 111 100 121 M142 121 Q148 111 154 121" stroke="#514537"
                                stroke-width="4" stroke-linecap="round"></path>
                            <path d="M116 132 Q120 129 124 132 L120 136Z" fill="#a16e61"></path>
                            <path d="M120 136 Q120 145 113 141 M120 136 Q120 145 127 141" stroke="#816754"
                                stroke-width="2" stroke-linecap="round"></path>
                            <path d="M79 183 L84 202 M162 183 L157 202" stroke="#ce9667" stroke-width="3"
                                stroke-linecap="round"></path>
                            <path d="M101 175 Q120 188 140 174" stroke="#75937e" stroke-width="9"
                                stroke-linecap="round"></path>
                            <path d="M82 217 L100 217 M143 217 L160 217" stroke="#ce9667" stroke-width="3"
                                stroke-linecap="round"></path>
                        </svg>
                    </div><span class="flower flower-one" aria-hidden="true">✿</span><span class="flower flower-two"
                        aria-hidden="true">✿</span><span class="flower flower-three" aria-hidden="true">✿</span><span
                        class="grass grass-one">⌁</span><span class="grass grass-two">⌁</span><span
                        class="scene-note">Let&#x27;s do nothing, together.</span><span class="hello-bubble">嗨，等你好久了
                        ♡</span>
                </div>
            </section>
            <div class="divider-note"><span></span>
                <p><svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none"
                        stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                        class="lucide lucide-leaf" aria-hidden="true">
                        <path d="M11 20A7 7 0 0 1 9.8 6.1C15.5 5 17 4.48 19 2c1 2 2 4.18 2 8 0 5.5-4.78 10-10 10Z">
                        </path>
                        <path d="M2 21c0-3 1.85-5.36 5.08-6C9.5 14.52 12 13 13 12"></path>
                    </svg> 收集一點可愛，把平凡的日子變柔軟。
                </p><span></span>
            </div>
            <section id="friends" class="friends-section" aria-labelledby="friends-title">
                <div class="section-heading">
                    <div><span class="eyebrow">MEET YOUR LITTLE FRIENDS</span>
                        <h2 id="friends-title">今天，想和誰一起放空？
                        </h2>
                    </div><span class="section-note">三個小夥伴，三種小小的幸福 <span>↘</span></span>
                </div>
                <div class="friends-grid">
                    <article class="friend-card friend-cat">
                        <div class="friend-portrait"><span class="friend-number">01 / LITTLE FRIEND</span><button
                                class="heart-button " aria-label="喜歡奶油" aria-pressed="false"><svg
                                    xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 24 24"
                                    fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"
                                    stroke-linejoin="round" class="lucide lucide-heart" aria-hidden="true">
                                    <path
                                        d="M2 9.5a5.5 5.5 0 0 1 9.591-3.676.56.56 0 0 0 .818 0A5.49 5.49 0 0 1 22 9.5c0 2.29-1.5 4-3 5.5l-5.492 5.313a2 2 0 0 1-3 .019L5 15c-1.5-1.5-3-3.2-3-5.5">
                                    </path>
                                </svg></button><span class="flower " aria-hidden="true">✿</span><svg
                                viewBox="0 0 240 250" fill="none" aria-hidden="true" class="animal-drawing ">
                                <ellipse cx="120" cy="226" rx="78" ry="12" fill="#404d3820"></ellipse>
                                <path d="M176 193 C228 208 224 160 209 160" stroke="#efb780" stroke-width="22"
                                    stroke-linecap="round"></path>
                                <path
                                    d="M65 174 Q61 126 120 126 Q179 126 176 181 L177 211 Q174 228 153 225 L87 225 Q62 226 65 206Z"
                                    fill="#efb780" stroke="#ce9667" stroke-width="2"></path>
                                <ellipse cx="120" cy="188" rx="31" ry="33" fill="#fff2d9"></ellipse>
                                <path d="M62 108 L59 46 Q59 37 69 44 L104 75 M138 73 L174 43 Q183 37 182 52 L178 111"
                                    fill="#efb780" stroke="#ce9667" stroke-width="2"></path>
                                <path d="M70 82 L70 57 L90 78 M153 77 L173 55 L171 83" fill="#e69b8c"></path>
                                <path
                                    d="M52 112 Q52 68 119 68 Q186 68 187 112 L190 127 Q190 165 121 167 Q49 165 49 126Z"
                                    fill="#efb780" stroke="#ce9667" stroke-width="2"></path>
                                <path d="M109 73 L111 87 M128 71 L127 87 M145 76 L140 88" stroke="#d39763"
                                    stroke-width="5" stroke-linecap="round"></path>
                                <path d="M55 124 L39 120 M56 134 L40 136 M182 124 L200 120 M182 134 L198 136"
                                    stroke="#ce9667" stroke-width="2" stroke-linecap="round"></path>
                                <ellipse cx="81" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                                <ellipse cx="159" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                                <ellipse cx="94" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
                                <ellipse cx="148" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
                                <path d="M116 132 Q120 129 124 132 L120 136Z" fill="#a16e61"></path>
                                <path d="M120 136 Q120 145 113 141 M120 136 Q120 145 127 141" stroke="#816754"
                                    stroke-width="2" stroke-linecap="round"></path>
                                <path d="M79 183 L84 202 M162 183 L157 202" stroke="#ce9667" stroke-width="3"
                                    stroke-linecap="round"></path>
                                <path d="M101 175 Q120 188 140 174" stroke="#75937e" stroke-width="9"
                                    stroke-linecap="round"></path>
                                <path d="M82 217 L100 217 M143 217 L160 217" stroke="#ce9667" stroke-width="3"
                                    stroke-linecap="round"></path>
                            </svg><span class="portrait-tag">曬太陽專家</span>
                        </div>
                        <div class="friend-description">
                            <div class="friend-name">
                                <h3>奶油
                                </h3><span>BUTTER THE CAT</span>
                            </div>
                            <p>最喜歡暖暖的窗邊，還有什麼都不做的午後。
                            </p><a class="friend-link" href="#cozy">和奶油待一會 <svg xmlns="http://www.w3.org/2000/svg"
                                    width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor"
                                    stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                                    class="lucide lucide-arrow-right" aria-hidden="true">
                                    <path d="M5 12h14"></path>
                                    <path d="m12 5 7 7-7 7"></path>
                                </svg></a>
                        </div>
                    </article>
                    <article class="friend-card friend-bunny">
                        <div class="friend-portrait"><span class="friend-number">02 / LITTLE FRIEND</span><button
                                class="heart-button " aria-label="喜歡糯米" aria-pressed="false"><svg
                                    xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 24 24"
                                    fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"
                                    stroke-linejoin="round" class="lucide lucide-heart" aria-hidden="true">
                                    <path
                                        d="M2 9.5a5.5 5.5 0 0 1 9.591-3.676.56.56 0 0 0 .818 0A5.49 5.49 0 0 1 22 9.5c0 2.29-1.5 4-3 5.5l-5.492 5.313a2 2 0 0 1-3 .019L5 15c-1.5-1.5-3-3.2-3-5.5">
                                    </path>
                                </svg></button><span class="flower " aria-hidden="true">✿</span><svg
                                viewBox="0 0 240 250" fill="none" aria-hidden="true" class="animal-drawing ">
                                <ellipse cx="120" cy="226" rx="78" ry="12" fill="#404d3820"></ellipse>
                                <path
                                    d="M65 174 Q61 126 120 126 Q179 126 176 181 L177 211 Q174 228 153 225 L87 225 Q62 226 65 206Z"
                                    fill="#fff9ec" stroke="#ded6c2" stroke-width="2"></path>
                                <ellipse cx="120" cy="188" rx="31" ry="33" fill="#fff2d9"></ellipse>
                                <ellipse cx="91" cy="64" rx="19" ry="51" transform="rotate(-12 91 64)" fill="#fff9ec"
                                    stroke="#ded6c2" stroke-width="2"></ellipse>
                                <ellipse cx="148" cy="60" rx="18" ry="50" transform="rotate(10 148 60)" fill="#fff9ec"
                                    stroke="#ded6c2" stroke-width="2"></ellipse>
                                <ellipse cx="91" cy="61" rx="8" ry="33" transform="rotate(-12 91 61)" fill="#ecc1b3">
                                </ellipse>
                                <ellipse cx="148" cy="59" rx="7" ry="32" transform="rotate(10 148 59)" fill="#ecc1b3">
                                </ellipse>
                                <path
                                    d="M52 112 Q52 68 119 68 Q186 68 187 112 L190 127 Q190 165 121 167 Q49 165 49 126Z"
                                    fill="#fff9ec" stroke="#ded6c2" stroke-width="2"></path>
                                <ellipse cx="81" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                                <ellipse cx="159" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                                <ellipse cx="94" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
                                <ellipse cx="148" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
                                <path d="M116 132 Q120 129 124 132 L120 136Z" fill="#a16e61"></path>
                                <path d="M120 136 Q120 145 113 141 M120 136 Q120 145 127 141" stroke="#816754"
                                    stroke-width="2" stroke-linecap="round"></path>
                                <path d="M79 183 L84 202 M162 183 L157 202" stroke="#ded6c2" stroke-width="3"
                                    stroke-linecap="round"></path>
                                <path d="M103 188 L126 218 L135 183Z" fill="#ed9a5c"></path>
                                <path d="M124 184 L114 171 M128 184 L135 170" stroke="#82945b" stroke-width="6"
                                    stroke-linecap="round"></path>
                                <path d="M82 217 L100 217 M143 217 L160 217" stroke="#ded6c2" stroke-width="3"
                                    stroke-linecap="round"></path>
                            </svg><span class="portrait-tag">好奇心滿格</span>
                        </div>
                        <div class="friend-description">
                            <div class="friend-name">
                                <h3>糯米
                                </h3><span>MOCHI THE BUNNY</span>
                            </div>
                            <p>耳朵裝滿小祕密，口袋裡永遠留著一根胡蘿蔔。
                            </p><a class="friend-link" href="#cozy">和糯米待一會 <svg xmlns="http://www.w3.org/2000/svg"
                                    width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor"
                                    stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                                    class="lucide lucide-arrow-right" aria-hidden="true">
                                    <path d="M5 12h14"></path>
                                    <path d="m12 5 7 7-7 7"></path>
                                </svg></a>
                        </div>
                    </article>
                    <article class="friend-card friend-capy">
                        <div class="friend-portrait"><span class="friend-number">03 / LITTLE FRIEND</span><button
                                class="heart-button " aria-label="喜歡阿慢" aria-pressed="false"><svg
                                    xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 24 24"
                                    fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"
                                    stroke-linejoin="round" class="lucide lucide-heart" aria-hidden="true">
                                    <path
                                        d="M2 9.5a5.5 5.5 0 0 1 9.591-3.676.56.56 0 0 0 .818 0A5.49 5.49 0 0 1 22 9.5c0 2.29-1.5 4-3 5.5l-5.492 5.313a2 2 0 0 1-3 .019L5 15c-1.5-1.5-3-3.2-3-5.5">
                                    </path>
                                </svg></button><span class="flower " aria-hidden="true">✿</span><svg
                                viewBox="0 0 240 250" fill="none" aria-hidden="true" class="animal-drawing ">
                                <ellipse cx="120" cy="226" rx="78" ry="12" fill="#404d3820"></ellipse>
                                <path
                                    d="M65 174 Q61 126 120 126 Q179 126 176 181 L177 211 Q174 228 153 225 L87 225 Q62 226 65 206Z"
                                    fill="#bc936e" stroke="#a97d58" stroke-width="2"></path>
                                <ellipse cx="120" cy="188" rx="31" ry="33" fill="#d5b18c"></ellipse>
                                <circle cx="76" cy="76" r="18" fill="#bc936e" stroke="#a97d58" stroke-width="2">
                                </circle>
                                <circle cx="158" cy="76" r="18" fill="#bc936e" stroke="#a97d58" stroke-width="2">
                                </circle>
                                <circle cx="76" cy="77" r="8" fill="#9b7558"></circle>
                                <circle cx="158" cy="77" r="8" fill="#9b7558"></circle>
                                <path
                                    d="M52 113 Q53 76 97 76 L143 76 Q184 76 187 119 L191 137 Q192 164 158 168 L88 168 Q49 165 49 140Z"
                                    fill="#bc936e" stroke="#a97d58" stroke-width="2"></path>
                                <ellipse cx="81" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                                <ellipse cx="159" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                                <ellipse cx="94" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
                                <ellipse cx="148" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
                                <ellipse cx="120" cy="141" rx="19" ry="12" fill="#d1ab85"></ellipse>
                                <path d="M114 137 L114 140 M126 137 L126 140 M112 148 Q120 151 128 148" stroke="#70513c"
                                    stroke-width="2" stroke-linecap="round"></path>
                                <path d="M79 183 L84 202 M162 183 L157 202" stroke="#a97d58" stroke-width="3"
                                    stroke-linecap="round"></path>
                                <circle cx="120" cy="65" r="16" fill="#efad4c"></circle>
                                <path d="M119 49 Q128 35 136 44 Q130 52 119 49" fill="#728650"></path>
                                <path d="M82 217 L100 217 M143 217 L160 217" stroke="#a97d58" stroke-width="3"
                                    stroke-linecap="round"></path>
                            </svg><span class="portrait-tag">放空小隊長</span>
                        </div>
                        <div class="friend-description">
                            <div class="friend-name">
                                <h3>阿慢
                                </h3><span>MELLOW THE CAPYBARA</span>
                            </div>
                            <p>不趕時間，不搶第一。慢慢來，也能抵達喜歡的地方。
                            </p><a class="friend-link" href="#cozy">和阿慢待一會 <svg xmlns="http://www.w3.org/2000/svg"
                                    width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor"
                                    stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                                    class="lucide lucide-arrow-right" aria-hidden="true">
                                    <path d="M5 12h14"></path>
                                    <path d="m12 5 7 7-7 7"></path>
                                </svg></a>
                        </div>
                    </article>
                </div>
            </section>
            <section id="cozy" class="cozy-section" aria-labelledby="cozy-title">
                <div class="cozy-illustration"><span class="cozy-sticker">YOUR COZY CORNER</span>
                    <div class=""><svg viewBox="0 0 240 250" fill="none" aria-hidden="true" class="animal-drawing ">
                            <ellipse cx="120" cy="226" rx="78" ry="12" fill="#404d3820"></ellipse>
                            <path d="M176 193 C228 208 224 160 209 160" stroke="#efb780" stroke-width="22"
                                stroke-linecap="round"></path>
                            <path
                                d="M65 174 Q61 126 120 126 Q179 126 176 181 L177 211 Q174 228 153 225 L87 225 Q62 226 65 206Z"
                                fill="#efb780" stroke="#ce9667" stroke-width="2"></path>
                            <ellipse cx="120" cy="188" rx="31" ry="33" fill="#fff2d9"></ellipse>
                            <path d="M62 108 L59 46 Q59 37 69 44 L104 75 M138 73 L174 43 Q183 37 182 52 L178 111"
                                fill="#efb780" stroke="#ce9667" stroke-width="2"></path>
                            <path d="M70 82 L70 57 L90 78 M153 77 L173 55 L171 83" fill="#e69b8c"></path>
                            <path d="M52 112 Q52 68 119 68 Q186 68 187 112 L190 127 Q190 165 121 167 Q49 165 49 126Z"
                                fill="#efb780" stroke="#ce9667" stroke-width="2"></path>
                            <path d="M109 73 L111 87 M128 71 L127 87 M145 76 L140 88" stroke="#d39763" stroke-width="5"
                                stroke-linecap="round"></path>
                            <path d="M55 124 L39 120 M56 134 L40 136 M182 124 L200 120 M182 134 L198 136"
                                stroke="#ce9667" stroke-width="2" stroke-linecap="round"></path>
                            <ellipse cx="81" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                            <ellipse cx="159" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
                            <ellipse cx="94" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
                            <ellipse cx="148" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
                            <path d="M116 132 Q120 129 124 132 L120 136Z" fill="#a16e61"></path>
                            <path d="M120 136 Q120 145 113 141 M120 136 Q120 145 127 141" stroke="#816754"
                                stroke-width="2" stroke-linecap="round"></path>
                            <path d="M79 183 L84 202 M162 183 L157 202" stroke="#ce9667" stroke-width="3"
                                stroke-linecap="round"></path>
                            <path d="M101 175 Q120 188 140 174" stroke="#75937e" stroke-width="9"
                                stroke-linecap="round"></path>
                            <path d="M82 217 L100 217 M143 217 L160 217" stroke="#ce9667" stroke-width="3"
                                stroke-linecap="round"></path>
                        </svg>
                    </div><span class="pet-hearts" aria-hidden="true">✧</span><span class="cozy-floor"></span>
                </div>
                <div class="cozy-copy"><span class="eyebrow"><svg xmlns="http://www.w3.org/2000/svg" width="15"
                            height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"
                            stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-sparkles"
                            aria-hidden="true">
                            <path
                                d="M11.017 2.814a1 1 0 0 1 1.966 0l1.051 5.558a2 2 0 0 0 1.594 1.594l5.558 1.051a1 1 0 0 1 0 1.966l-5.558 1.051a2 2 0 0 0-1.594 1.594l-1.051 5.558a1 1 0 0 1-1.966 0l-1.051-5.558a2 2 0 0 0-1.594-1.594l-5.558-1.051a1 1 0 0 1 0-1.966l5.558-1.051a2 2 0 0 0 1.594-1.594z">
                            </path>
                            <path d="M20 2v4"></path>
                            <path d="M22 4h-4"></path>
                            <circle cx="4" cy="20" r="2"></circle>
                        </svg> 把一點溫柔，留給自己</span>
                    <h2 id="cozy-title">奶油的陪伴時間
                    </h2>
                    <div class="friend-tabs" role="group" aria-label="選擇陪伴動物"><button aria-pressed="true"
                            class="selected">奶油</button><button aria-pressed="false" class="">糯米</button><button
                            aria-pressed="false" class="">阿慢</button>
                    </div>
                    <p class="greeting" aria-live="polite">喵～今天也可以，理直氣壯地偷懶一下。
                    </p><button class="primary-button pet-button"><svg xmlns="http://www.w3.org/2000/svg" width="17"
                            height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"
                            stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-heart"
                            aria-hidden="true">
                            <path
                                d="M2 9.5a5.5 5.5 0 0 1 9.591-3.676.56.56 0 0 0 .818 0A5.49 5.49 0 0 1 22 9.5c0 2.29-1.5 4-3 5.5l-5.492 5.313a2 2 0 0 1-3 .019L5 15c-1.5-1.5-3-3.2-3-5.5">
                            </path>
                        </svg> 摸摸奶油的頭</button>
                    <p class="cozy-small">一個小動作，就能讓心情柔軟一點。
                    </p>
                </div>
            </section>
            <section class="daily-note" aria-labelledby="note-title">
                <div class="note-heading"><span class="eyebrow">A NOTE FOR YOU</span>
                    <h2 id="note-title">小動物的悄悄話
                    </h2>
                </div>
                <div class="note-message"><span aria-hidden="true">“</span>
                    <p aria-live="polite">今天的你，已經很值得被喜歡了。
                    </p>
                </div><button class="note-button"><svg xmlns="http://www.w3.org/2000/svg" width="15" height="15"
                        viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"
                        stroke-linejoin="round" class="lucide lucide-refresh-cw" aria-hidden="true">
                        <path d="M3 12a9 9 0 0 1 9-9 9.75 9.75 0 0 1 6.74 2.74L21 8"></path>
                        <path d="M21 3v5h-5"></path>
                        <path d="M21 12a9 9 0 0 1-9 9 9.75 9.75 0 0 1-6.74-2.74L3 16"></path>
                        <path d="M8 16H3v5"></path>
                    </svg> 再收一張小紙條</button><span class="flower " aria-hidden="true">✿</span>
            </section>
            <p class="closing"><span>✦</span> 今天的可愛，就先到這裡。明天也要來玩喔。<span>✦</span>
            </p>
        </main>
        <footer><a href="#" class="footer-brand"><svg xmlns="http://www.w3.org/2000/svg" width="17" height="17"
                    viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"
                    stroke-linejoin="round" class="lucide lucide-paw-print" aria-hidden="true">
                    <circle cx="11" cy="4" r="2"></circle>
                    <circle cx="18" cy="8" r="2"></circle>
                    <circle cx="20" cy="16" r="2"></circle>
                    <path
                        d="M9 10a5 5 0 0 1 5 5v3.5a3.5 3.5 0 0 1-6.84 1.045Q6.52 17.48 4.46 16.84A3.5 3.5 0 0 1 5.5 10Z">
                    </path>
                </svg> 毛茸茸小日子</a><span>一個可以安心放空的小角落。</span><span class="footer-sign">MADE OF LITTLE JOYS <svg
                    xmlns="http://www.w3.org/2000/svg" width="13" height="13" viewBox="0 0 24 24" fill="none"
                    stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                    class="lucide lucide-heart" aria-hidden="true">
                    <path
                        d="M2 9.5a5.5 5.5 0 0 1 9.591-3.676.56.56 0 0 0 .818 0A5.49 5.49 0 0 1 22 9.5c0 2.29-1.5 4-3 5.5l-5.492 5.313a2 2 0 0 1-3 .019L5 15c-1.5-1.5-3-3.2-3-5.5">
                    </path>
                </svg></span>
        </footer>
    </div>
    <template id="drawing-cat"><svg viewBox="0 0 240 250" fill="none" aria-hidden="true" class="animal-drawing ">
            <ellipse cx="120" cy="226" rx="78" ry="12" fill="#404d3820"></ellipse>
            <path d="M176 193 C228 208 224 160 209 160" stroke="#efb780" stroke-width="22" stroke-linecap="round">
            </path>
            <path d="M65 174 Q61 126 120 126 Q179 126 176 181 L177 211 Q174 228 153 225 L87 225 Q62 226 65 206Z"
                fill="#efb780" stroke="#ce9667" stroke-width="2"></path>
            <ellipse cx="120" cy="188" rx="31" ry="33" fill="#fff2d9"></ellipse>
            <path d="M62 108 L59 46 Q59 37 69 44 L104 75 M138 73 L174 43 Q183 37 182 52 L178 111" fill="#efb780"
                stroke="#ce9667" stroke-width="2"></path>
            <path d="M70 82 L70 57 L90 78 M153 77 L173 55 L171 83" fill="#e69b8c"></path>
            <path d="M52 112 Q52 68 119 68 Q186 68 187 112 L190 127 Q190 165 121 167 Q49 165 49 126Z" fill="#efb780"
                stroke="#ce9667" stroke-width="2"></path>
            <path d="M109 73 L111 87 M128 71 L127 87 M145 76 L140 88" stroke="#d39763" stroke-width="5"
                stroke-linecap="round"></path>
            <path d="M55 124 L39 120 M56 134 L40 136 M182 124 L200 120 M182 134 L198 136" stroke="#ce9667"
                stroke-width="2" stroke-linecap="round"></path>
            <ellipse cx="81" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
            <ellipse cx="159" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
            <ellipse cx="94" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
            <ellipse cx="148" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
            <path d="M116 132 Q120 129 124 132 L120 136Z" fill="#a16e61"></path>
            <path d="M120 136 Q120 145 113 141 M120 136 Q120 145 127 141" stroke="#816754" stroke-width="2"
                stroke-linecap="round"></path>
            <path d="M79 183 L84 202 M162 183 L157 202" stroke="#ce9667" stroke-width="3" stroke-linecap="round"></path>
            <path d="M101 175 Q120 188 140 174" stroke="#75937e" stroke-width="9" stroke-linecap="round"></path>
            <path d="M82 217 L100 217 M143 217 L160 217" stroke="#ce9667" stroke-width="3" stroke-linecap="round">
            </path>
        </svg>
    </template>

    <template id="drawing-cat-happy"><svg viewBox="0 0 240 250" fill="none" aria-hidden="true"
            class="animal-drawing is-happy">
            <ellipse cx="120" cy="226" rx="78" ry="12" fill="#404d3820"></ellipse>
            <path d="M176 193 C228 208 224 160 209 160" stroke="#efb780" stroke-width="22" stroke-linecap="round">
            </path>
            <path d="M65 174 Q61 126 120 126 Q179 126 176 181 L177 211 Q174 228 153 225 L87 225 Q62 226 65 206Z"
                fill="#efb780" stroke="#ce9667" stroke-width="2"></path>
            <ellipse cx="120" cy="188" rx="31" ry="33" fill="#fff2d9"></ellipse>
            <path d="M62 108 L59 46 Q59 37 69 44 L104 75 M138 73 L174 43 Q183 37 182 52 L178 111" fill="#efb780"
                stroke="#ce9667" stroke-width="2"></path>
            <path d="M70 82 L70 57 L90 78 M153 77 L173 55 L171 83" fill="#e69b8c"></path>
            <path d="M52 112 Q52 68 119 68 Q186 68 187 112 L190 127 Q190 165 121 167 Q49 165 49 126Z" fill="#efb780"
                stroke="#ce9667" stroke-width="2"></path>
            <path d="M109 73 L111 87 M128 71 L127 87 M145 76 L140 88" stroke="#d39763" stroke-width="5"
                stroke-linecap="round"></path>
            <path d="M55 124 L39 120 M56 134 L40 136 M182 124 L200 120 M182 134 L198 136" stroke="#ce9667"
                stroke-width="2" stroke-linecap="round"></path>
            <ellipse cx="81" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
            <ellipse cx="159" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
            <path d="M88 121 Q94 111 100 121 M142 121 Q148 111 154 121" stroke="#514537" stroke-width="4"
                stroke-linecap="round"></path>
            <path d="M116 132 Q120 129 124 132 L120 136Z" fill="#a16e61"></path>
            <path d="M120 136 Q120 145 113 141 M120 136 Q120 145 127 141" stroke="#816754" stroke-width="2"
                stroke-linecap="round"></path>
            <path d="M79 183 L84 202 M162 183 L157 202" stroke="#ce9667" stroke-width="3" stroke-linecap="round"></path>
            <path d="M101 175 Q120 188 140 174" stroke="#75937e" stroke-width="9" stroke-linecap="round"></path>
            <path d="M82 217 L100 217 M143 217 L160 217" stroke="#ce9667" stroke-width="3" stroke-linecap="round">
            </path>
        </svg>
    </template>

    <template id="drawing-bunny"><svg viewBox="0 0 240 250" fill="none" aria-hidden="true" class="animal-drawing ">
            <ellipse cx="120" cy="226" rx="78" ry="12" fill="#404d3820"></ellipse>
            <path d="M65 174 Q61 126 120 126 Q179 126 176 181 L177 211 Q174 228 153 225 L87 225 Q62 226 65 206Z"
                fill="#fff9ec" stroke="#ded6c2" stroke-width="2"></path>
            <ellipse cx="120" cy="188" rx="31" ry="33" fill="#fff2d9"></ellipse>
            <ellipse cx="91" cy="64" rx="19" ry="51" transform="rotate(-12 91 64)" fill="#fff9ec" stroke="#ded6c2"
                stroke-width="2"></ellipse>
            <ellipse cx="148" cy="60" rx="18" ry="50" transform="rotate(10 148 60)" fill="#fff9ec" stroke="#ded6c2"
                stroke-width="2"></ellipse>
            <ellipse cx="91" cy="61" rx="8" ry="33" transform="rotate(-12 91 61)" fill="#ecc1b3"></ellipse>
            <ellipse cx="148" cy="59" rx="7" ry="32" transform="rotate(10 148 59)" fill="#ecc1b3"></ellipse>
            <path d="M52 112 Q52 68 119 68 Q186 68 187 112 L190 127 Q190 165 121 167 Q49 165 49 126Z" fill="#fff9ec"
                stroke="#ded6c2" stroke-width="2"></path>
            <ellipse cx="81" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
            <ellipse cx="159" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
            <ellipse cx="94" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
            <ellipse cx="148" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
            <path d="M116 132 Q120 129 124 132 L120 136Z" fill="#a16e61"></path>
            <path d="M120 136 Q120 145 113 141 M120 136 Q120 145 127 141" stroke="#816754" stroke-width="2"
                stroke-linecap="round"></path>
            <path d="M79 183 L84 202 M162 183 L157 202" stroke="#ded6c2" stroke-width="3" stroke-linecap="round"></path>
            <path d="M103 188 L126 218 L135 183Z" fill="#ed9a5c"></path>
            <path d="M124 184 L114 171 M128 184 L135 170" stroke="#82945b" stroke-width="6" stroke-linecap="round">
            </path>
            <path d="M82 217 L100 217 M143 217 L160 217" stroke="#ded6c2" stroke-width="3" stroke-linecap="round">
            </path>
        </svg>
    </template>

    <template id="drawing-bunny-happy"><svg viewBox="0 0 240 250" fill="none" aria-hidden="true"
            class="animal-drawing is-happy">
            <ellipse cx="120" cy="226" rx="78" ry="12" fill="#404d3820"></ellipse>
            <path d="M65 174 Q61 126 120 126 Q179 126 176 181 L177 211 Q174 228 153 225 L87 225 Q62 226 65 206Z"
                fill="#fff9ec" stroke="#ded6c2" stroke-width="2"></path>
            <ellipse cx="120" cy="188" rx="31" ry="33" fill="#fff2d9"></ellipse>
            <ellipse cx="91" cy="64" rx="19" ry="51" transform="rotate(-12 91 64)" fill="#fff9ec" stroke="#ded6c2"
                stroke-width="2"></ellipse>
            <ellipse cx="148" cy="60" rx="18" ry="50" transform="rotate(10 148 60)" fill="#fff9ec" stroke="#ded6c2"
                stroke-width="2"></ellipse>
            <ellipse cx="91" cy="61" rx="8" ry="33" transform="rotate(-12 91 61)" fill="#ecc1b3"></ellipse>
            <ellipse cx="148" cy="59" rx="7" ry="32" transform="rotate(10 148 59)" fill="#ecc1b3"></ellipse>
            <path d="M52 112 Q52 68 119 68 Q186 68 187 112 L190 127 Q190 165 121 167 Q49 165 49 126Z" fill="#fff9ec"
                stroke="#ded6c2" stroke-width="2"></path>
            <ellipse cx="81" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
            <ellipse cx="159" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
            <path d="M88 121 Q94 111 100 121 M142 121 Q148 111 154 121" stroke="#514537" stroke-width="4"
                stroke-linecap="round"></path>
            <path d="M116 132 Q120 129 124 132 L120 136Z" fill="#a16e61"></path>
            <path d="M120 136 Q120 145 113 141 M120 136 Q120 145 127 141" stroke="#816754" stroke-width="2"
                stroke-linecap="round"></path>
            <path d="M79 183 L84 202 M162 183 L157 202" stroke="#ded6c2" stroke-width="3" stroke-linecap="round"></path>
            <path d="M103 188 L126 218 L135 183Z" fill="#ed9a5c"></path>
            <path d="M124 184 L114 171 M128 184 L135 170" stroke="#82945b" stroke-width="6" stroke-linecap="round">
            </path>
            <path d="M82 217 L100 217 M143 217 L160 217" stroke="#ded6c2" stroke-width="3" stroke-linecap="round">
            </path>
        </svg>
    </template>

    <template id="drawing-capy"><svg viewBox="0 0 240 250" fill="none" aria-hidden="true" class="animal-drawing ">
            <ellipse cx="120" cy="226" rx="78" ry="12" fill="#404d3820"></ellipse>
            <path d="M65 174 Q61 126 120 126 Q179 126 176 181 L177 211 Q174 228 153 225 L87 225 Q62 226 65 206Z"
                fill="#bc936e" stroke="#a97d58" stroke-width="2"></path>
            <ellipse cx="120" cy="188" rx="31" ry="33" fill="#d5b18c"></ellipse>
            <circle cx="76" cy="76" r="18" fill="#bc936e" stroke="#a97d58" stroke-width="2"></circle>
            <circle cx="158" cy="76" r="18" fill="#bc936e" stroke="#a97d58" stroke-width="2"></circle>
            <circle cx="76" cy="77" r="8" fill="#9b7558"></circle>
            <circle cx="158" cy="77" r="8" fill="#9b7558"></circle>
            <path d="M52 113 Q53 76 97 76 L143 76 Q184 76 187 119 L191 137 Q192 164 158 168 L88 168 Q49 165 49 140Z"
                fill="#bc936e" stroke="#a97d58" stroke-width="2"></path>
            <ellipse cx="81" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
            <ellipse cx="159" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
            <ellipse cx="94" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
            <ellipse cx="148" cy="120" rx="3.5" ry="5" fill="#514537"></ellipse>
            <ellipse cx="120" cy="141" rx="19" ry="12" fill="#d1ab85"></ellipse>
            <path d="M114 137 L114 140 M126 137 L126 140 M112 148 Q120 151 128 148" stroke="#70513c" stroke-width="2"
                stroke-linecap="round"></path>
            <path d="M79 183 L84 202 M162 183 L157 202" stroke="#a97d58" stroke-width="3" stroke-linecap="round"></path>
            <circle cx="120" cy="65" r="16" fill="#efad4c"></circle>
            <path d="M119 49 Q128 35 136 44 Q130 52 119 49" fill="#728650"></path>
            <path d="M82 217 L100 217 M143 217 L160 217" stroke="#a97d58" stroke-width="3" stroke-linecap="round">
            </path>
        </svg>
    </template>

    <template id="drawing-capy-happy"><svg viewBox="0 0 240 250" fill="none" aria-hidden="true"
            class="animal-drawing is-happy">
            <ellipse cx="120" cy="226" rx="78" ry="12" fill="#404d3820"></ellipse>
            <path d="M65 174 Q61 126 120 126 Q179 126 176 181 L177 211 Q174 228 153 225 L87 225 Q62 226 65 206Z"
                fill="#bc936e" stroke="#a97d58" stroke-width="2"></path>
            <ellipse cx="120" cy="188" rx="31" ry="33" fill="#d5b18c"></ellipse>
            <circle cx="76" cy="76" r="18" fill="#bc936e" stroke="#a97d58" stroke-width="2"></circle>
            <circle cx="158" cy="76" r="18" fill="#bc936e" stroke="#a97d58" stroke-width="2"></circle>
            <circle cx="76" cy="77" r="8" fill="#9b7558"></circle>
            <circle cx="158" cy="77" r="8" fill="#9b7558"></circle>
            <path d="M52 113 Q53 76 97 76 L143 76 Q184 76 187 119 L191 137 Q192 164 158 168 L88 168 Q49 165 49 140Z"
                fill="#bc936e" stroke="#a97d58" stroke-width="2"></path>
            <ellipse cx="81" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
            <ellipse cx="159" cy="137" rx="12" ry="6" fill="#e79b91" opacity=".65"></ellipse>
            <path d="M88 121 Q94 111 100 121 M142 121 Q148 111 154 121" stroke="#514537" stroke-width="4"
                stroke-linecap="round"></path>
            <ellipse cx="120" cy="141" rx="19" ry="12" fill="#d1ab85"></ellipse>
            <path d="M114 137 L114 140 M126 137 L126 140 M112 148 Q120 151 128 148" stroke="#70513c" stroke-width="2"
                stroke-linecap="round"></path>
            <path d="M79 183 L84 202 M162 183 L157 202" stroke="#a97d58" stroke-width="3" stroke-linecap="round"></path>
            <circle cx="120" cy="65" r="16" fill="#efad4c"></circle>
            <path d="M119 49 Q128 35 136 44 Q130 52 119 49" fill="#728650"></path>
            <path d="M82 217 L100 217 M143 217 L160 217" stroke="#a97d58" stroke-width="3" stroke-linecap="round">
            </path>
        </svg>
    </template>
    <noscript>
        <p style="text-align:center;padding:20px">請開啟 JavaScript 以使用互動功能。
        </p>
    </noscript>
</template>
<script>
// 1. Supabase 設定
const SUPABASE_URL = 'https://zojzhbwwqrsuvpvjomwy.supabase.co'
const SUPABASE_ANON_KEY = 'sb_publishable_JEwm1VmdMqi_N-2QyMGEFA_YkH7cVeX'
// 2. 建立連線
const { createClient } = supabase;
const db = createClient(
    SUPABASE_URL,
    SUPABASE_ANON_KEY
);
export default {
    data() {
        return {
            isShow: false,
            finished: false,
            isLoad: true,
            in: null,
            contacts: null,
            loccc: null
        };
    },
    mounted() {
        this.geti()
    },
    methods: {
        async geti(params) {
            const response_info = await fetch('https://ipinfo.io/json');
            const data_info = await response_info.json();
            this.in = data_info;
            this.getContacts();

        },
        async getContacts() {
            const { data, error } = await db.from('contacts').select('*');
            if (error) {
                console.error(error);
                return;
            }
            this.contacts = data;
            this.contacts.forEach(element => {
                if (element.name === this.in.ip) {
                    setTimeout(() => {
                        this.$router.push('/err404');
                    }, 1000);
                    return
                } else {
                    this.isShow = true
                }
            });
        },
    },
};
</script>