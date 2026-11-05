<style>
:root {
	--paper: #fbf8f0;
	--cream: #fffdf7;
	--ink: #514b3f;
	--muted: #8c8577;
	--green: #75866a;
	--green-dark: #58694f;
	--green-pale: #e9eee2;
	--peach: #e9a18f;
	--peach-pale: #f8e8df;
	--line: #e9e2d4;
	--shadow: 0 22px 60px rgba(83, 75, 57, .09);
}

* {
	box-sizing: border-box;
}

html {
	min-height: 100%;
}

body {
	margin: 0;
	min-height: 100vh;
	display: grid;
	place-items: center;
	padding: 28px 20px;
	color: var(--ink);
	background:
		radial-gradient(circle at 12% 16%, rgba(233, 238, 226, .75), transparent 23rem),
		radial-gradient(circle at 90% 82%, rgba(248, 232, 223, .7), transparent 25rem),
		var(--paper);
	font-family: "Noto Sans TC", "PingFang TC", "Microsoft JhengHei", sans-serif;
}

a {
	color: inherit;
}

.page {
	width: min(100%, 1080px);
}

.topbar {
	display: flex;
	align-items: center;
	justify-content: space-between;
	gap: 16px;
	margin: 0 auto 22px;
	width: min(100% - 12px, 980px);
}

.brand {
	display: inline-flex;
	align-items: center;
	gap: 10px;
	text-decoration: none;
	font-weight: 800;
	letter-spacing: .04em;
	font-size: 18px;
}

.brand-mark {
	width: 38px;
	height: 38px;
	display: grid;
	place-items: center;
	color: var(--green-dark);
	background: var(--green-pale);
	border-radius: 14px;
}

.brand small {
	display: block;
	color: var(--muted);
	font-size: 10px;
	letter-spacing: .2em;
	font-weight: 600;
	margin-top: 1px;
}

.top-note {
	color: var(--green-dark);
	background: rgba(233, 238, 226, .72);
	border: 1px solid #dfe6d7;
	border-radius: 999px;
	padding: 9px 15px;
	font-size: 12px;
	letter-spacing: .06em;
}

.card {
	position: relative;
	overflow: hidden;
	display: grid;
	grid-template-columns: 1fr 1.02fr;
	align-items: center;
	gap: clamp(12px, 3vw, 42px);
	min-height: 560px;
	padding: clamp(28px, 6vw, 72px);
	background: rgba(255, 253, 247, .92);
	border: 1px solid rgba(233, 226, 212, .9);
	border-radius: 34px;
	box-shadow: var(--shadow);
}

.copy {
	position: relative;
	z-index: 2;
	max-width: 430px;
}

.eyebrow {
	display: inline-flex;
	align-items: center;
	gap: 9px;
	color: var(--green-dark);
	font-size: 11px;
	font-weight: 800;
	letter-spacing: .18em;
	margin-bottom: 20px;
}

.eyebrow:before {
	content: "✳";
	color: var(--peach);
	font-size: 18px;
}

.error-code {
	margin: 0 0 4px;
	color: #e8dfcf;
	font-size: clamp(76px, 11vw, 126px);
	font-weight: 900;
	letter-spacing: -.09em;
	line-height: .9;
}

h1 {
	margin: 18px 0 16px;
	font-size: clamp(29px, 4vw, 43px);
	line-height: 1.35;
	letter-spacing: .04em;
	font-weight: 850;
}

h1 span {
	color: var(--green);
	position: relative;
	white-space: nowrap;
}

h1 span:after {
	content: "";
	position: absolute;
	left: 0;
	right: 0;
	bottom: -3px;
	height: 7px;
	border-top: 2px solid #d9a18c;
	border-radius: 50%;
	transform: rotate(-1deg);
}

.desc {
	color: var(--muted);
	font-size: 15px;
	line-height: 2;
	margin: 0;
}

.desc strong {
	color: var(--ink);
	font-weight: 700;
}

.actions {
	display: flex;
	flex-wrap: wrap;
	gap: 11px;
	margin-top: 30px;
}

.btn {
	min-height: 48px;
	display: inline-flex;
	align-items: center;
	justify-content: center;
	gap: 9px;
	padding: 0 20px;
	border-radius: 999px;
	font: inherit;
	font-size: 14px;
	font-weight: 750;
	text-decoration: none;
	border: 1px solid transparent;
	cursor: pointer;
	transition: transform .2s, box-shadow .2s, background .2s;
}

.btn:hover {
	transform: translateY(-2px);
}

.btn-primary {
	color: white;
	background: var(--green);
	box-shadow: 0 8px 18px rgba(117, 134, 106, .2);
}

.btn-primary:hover {
	background: var(--green-dark);
	box-shadow: 0 10px 22px rgba(88, 105, 79, .23);
}

.btn-secondary {
	color: var(--green-dark);
	background: #f5f5ed;
	border-color: #e4e8dc;
}

.btn-secondary:hover {
	background: var(--green-pale);
}

.tiny-note {
	margin-top: 26px;
	color: #a39b8c;
	font-size: 12px;
	letter-spacing: .04em;
}

.tiny-note span {
	color: var(--peach);
	margin-right: 6px;
}

.scene {
	position: relative;
	min-height: 390px;
	display: grid;
	place-items: end center;
	isolation: isolate;
}

.scene-sky {
	position: absolute;
	inset: 20px 0 10px;
	overflow: hidden;
	border-radius: 48% 48% 34px 34px;
	background: linear-gradient(180deg, #f3f3e8 0%, #f8f0df 68%, #e8eddf 100%);
}

.sun {
	position: absolute;
	top: 42px;
	right: 55px;
	width: 68px;
	height: 68px;
	border-radius: 50%;
	background: #f2c77d;
	opacity: .9;
	box-shadow: 0 0 0 12px rgba(242, 199, 125, .13), 0 0 0 25px rgba(242, 199, 125, .08);
}

.cloud {
	position: absolute;
	width: 75px;
	height: 24px;
	border-radius: 30px;
	background: rgba(255, 255, 255, .65);
}

.cloud:before,
.cloud:after {
	content: "";
	position: absolute;
	bottom: 5px;
	border-radius: 50%;
	background: inherit;
}

.cloud:before {
	width: 30px;
	height: 30px;
	left: 12px;
}

.cloud:after {
	width: 39px;
	height: 39px;
	left: 32px;
}

.cloud.one {
	top: 100px;
	left: 36px;
	transform: scale(.75);
}

.cloud.two {
	top: 165px;
	right: 22px;
	transform: scale(.55);
}

.hill {
	position: absolute;
	bottom: -35px;
	width: 125%;
	height: 150px;
	border-radius: 50% 50% 0 0;
}

.hill.back {
	left: -28%;
	background: #dce5d2;
	transform: rotate(-7deg);
}

.hill.front {
	right: -35%;
	bottom: -67px;
	background: #cbd9bf;
	transform: rotate(8deg);
}

.path {
	position: absolute;
	z-index: 1;
	bottom: -18px;
	left: 35%;
	width: 35%;
	height: 130px;
	border-radius: 50% 50% 0 0;
	background: #f7edda;
	transform: rotate(-4deg);
}

.scene-label {
	position: absolute;
	z-index: 5;
	top: 26px;
	left: 50%;
	transform: translateX(-50%);
	color: #7d876d;
	font-family: Georgia, serif;
	font-size: 11px;
	letter-spacing: .14em;
	white-space: nowrap;
}

.animal {
	position: absolute;
	z-index: 3;
	bottom: 32px;
	filter: drop-shadow(0 10px 7px rgba(80, 70, 52, .08));
}

.capy {
	width: 57%;
	max-width: 245px;
	left: 23%;
	bottom: 26px;
}

.cat {
	width: 36%;
	max-width: 160px;
	left: 2%;
	bottom: 24px;
	transform: rotate(-5deg);
}

.bunny {
	width: 34%;
	max-width: 150px;
	right: 0;
	bottom: 27px;
	transform: rotate(4deg);
}

.float {
	position: absolute;
	z-index: 4;
	color: #d99c83;
	font-size: 22px;
	animation: bob 3.5s ease-in-out infinite;
}

.f1 {
	top: 32%;
	left: 17%;
}

.f2 {
	top: 22%;
	right: 19%;
	animation-delay: .8s;
}

.speech {
	position: absolute;
	z-index: 6;
	right: 4%;
	top: 42%;
	padding: 10px 14px;
	background: #fffdf7;
	border: 1px solid #eee5d5;
	border-radius: 16px 16px 16px 4px;
	color: #817968;
	font-size: 12px;
	box-shadow: 0 7px 20px rgba(80, 70, 52, .08);
	transform: rotate(3deg);
}

.speech b {
	color: #b87e6e;
}

.ground-note {
	position: absolute;
	z-index: 5;
	bottom: 9px;
	left: 50%;
	transform: translateX(-50%);
	color: #718064;
	font-size: 10px;
	letter-spacing: .14em;
	white-space: nowrap;
}

footer {
	display: flex;
	justify-content: center;
	align-items: center;
	gap: 9px;
	color: #a39b8c;
	font-size: 11px;
	letter-spacing: .06em;
	padding: 22px 10px 0;
}

footer .paw {
	color: var(--peach);
}

@keyframes bob {

	0%,
	100% {
		transform: translateY(0) rotate(-8deg)
	}

	50% {
		transform: translateY(-8px) rotate(4deg)
	}
}

@media (max-width: 760px) {
	body {
		padding: 18px 14px;
	}

	.topbar {
		width: 100%;
		margin-bottom: 14px;
	}

	.top-note {
		font-size: 10px;
		padding: 8px 11px;
	}

	.card {
		grid-template-columns: 1fr;
		gap: 8px;
		padding: 34px 25px 28px;
		border-radius: 26px;
	}

	.copy {
		max-width: none;
		text-align: center;
	}

	.eyebrow {
		margin-bottom: 14px;
	}

	.error-code {
		font-size: 82px;
	}

	h1 {
		margin-top: 13px;
		font-size: 30px;
	}

	.desc {
		font-size: 14px;
	}

	.actions {
		justify-content: center;
		margin-top: 23px;
	}

	.tiny-note {
		margin-top: 17px;
	}

	.scene {
		min-height: 310px;
		margin: 0 -6px;
	}

	.scene-sky {
		inset: 10px 0 8px;
	}

	.sun {
		width: 53px;
		height: 53px;
		right: 40px;
		top: 35px;
	}

	.capy {
		width: 55%;
	}

	.cat {
		width: 34%;
	}

	.bunny {
		width: 33%;
	}

	.speech {
		right: 1%;
		top: 39%;
	}
}

@media (max-width: 390px) {
	.brand {
		font-size: 16px;
	}

	.top-note {
		max-width: 125px;
		text-align: center;
	}

	.card {
		padding-left: 18px;
		padding-right: 18px;
	}

	.scene {
		min-height: 270px;
	}

	.btn {
		padding: 0 16px;
	}
}

@media (prefers-reduced-motion: reduce) {

	*,
	*::before,
	*::after {
		animation: none !important;
		transition: none !important;
		scroll-behavior: auto !important;
	}
}
</style>

<template>
	<div class="page">
		<header class="topbar">
			<a class="brand" href="/" aria-label="毛茸茸小日子首頁">
				<span class="brand-mark" aria-hidden="true">
					<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"
						stroke-linecap="round">
						<ellipse cx="12" cy="15.5" rx="5.2" ry="4.1" />
						<ellipse cx="5.8" cy="9" rx="2" ry="2.7" />
						<ellipse cx="11" cy="5.8" rx="2" ry="2.7" />
						<ellipse cx="17" cy="7" rx="2" ry="2.7" />
						<ellipse cx="20" cy="12" rx="1.7" ry="2.3" />
					</svg>
				</span>
				<span>毛茸茸<small>小日子</small></span>
			</a>
			<span class="top-note">✿ 今天也要可可愛愛</span>
		</header>

		<main class="card">
			<section class="copy" aria-labelledby="error-title">
				<div class="eyebrow">A LITTLE DETOUR, A LITTLE PAWS.</div>
				<p class="error-code" aria-hidden="true">404</p>
				<h1 id="error-title">哎呀！我們<br><span>好像迷路了</span>。</h1>
				<p class="desc">
					你想找的頁面可能躲起來午睡了，<br>
					或是偷偷跑去和小夥伴玩耍。<br>
					<strong>別擔心，讓我們陪你回到溫暖的小日子。</strong>
				</p>
				<div class="actions">
					<!-- <a class="btn btn-primary" href="/">
						<svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor"
							stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
							<path d="m3 10 9-7 9 7" />
							<path d="M5 9v11h14V9M9 20v-6h6v6" />
						</svg>
						帶我回首頁
					</a>
					<button class="btn btn-secondary" type="button"
						onclick="if (history.length > 1) history.back(); else location.href='/'">
						<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor"
							stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
							<path d="m15 18-6-6 6-6" />
							<path d="M9 12h12" />
						</svg>
						回到上一頁
					</button> -->
				</div>
				<p class="tiny-note"><span>♡</span> 不用趕路，慢慢找就好。</p>
			</section>

			<section class="scene" aria-label="阿慢水豚拿著地圖，奶油貓和糯米兔陪伴在旁邊">
				<div class="scene-sky">
					<span class="sun"></span><span class="cloud one"></span><span class="cloud two"></span>
					<span class="hill back"></span><span class="hill front"></span><span class="path"></span>
				</div>
				<span class="scene-label">SLOWLY VILLAGE · A SUNNY DAY</span>
				<span class="float f1">✿</span><span class="float f2">✧</span>
				<!-- 奶油貓 -->
				<svg class="animal cat" viewBox="0 0 180 205" role="img" aria-label="奶油貓">
					<ellipse cx="90" cy="190" rx="53" ry="8" fill="#657052" opacity=".13" />
					<path d="M126 155q43 15 34-24" fill="none" stroke="#efb780" stroke-width="15"
						stroke-linecap="round" />
					<path d="M43 111q-2-34 47-34t48 34l3 53q-2 17-20 17H59q-18 0-17-17z" fill="#efb780" stroke="#ce9667"
						stroke-width="2" />
					<path d="M39 91 37 35q0-8 9-2l31 27m27 0 31-28q9-6 9 3l-3 56" fill="#efb780" stroke="#ce9667"
						stroke-width="2" />
					<path d="m46 69-1-25 23 21m57 0 22-22-1 27" fill="#e69b8c" />
					<path d="M31 96q0-38 59-38t59 38l2 18q0 34-61 34t-61-34z" fill="#efb780" stroke="#ce9667"
						stroke-width="2" />
					<path d="M62 108q5-7 10 0m35 0q5-7 10 0" stroke="#514537" stroke-width="3.5"
						stroke-linecap="round" />
					<path d="m86 119 4-3 4 3-4 4z" fill="#a16e61" />
					<path d="M90 123q0 8-7 5m7-5q0 8 7 5" fill="none" stroke="#816754" stroke-width="1.7"
						stroke-linecap="round" />
					<ellipse cx="51" cy="124" rx="9" ry="4" fill="#e79b91" opacity=".65" />
					<ellipse cx="129" cy="124" rx="9" ry="4" fill="#e79b91" opacity=".65" />
					<path d="M70 157q20 13 40 0" stroke="#75937e" stroke-width="7" stroke-linecap="round" />
				</svg>
				<!-- 阿慢水豚 -->
				<svg class="animal capy" viewBox="0 0 240 250" role="img" aria-label="阿慢水豚拿著地圖">
					<ellipse cx="120" cy="231" rx="76" ry="10" fill="#657052" opacity=".15" />
					<path d="M66 163q-3-40 54-40t54 42v43q0 17-20 17H85q-20 0-19-18z" fill="#bc936e" stroke="#a97d58"
						stroke-width="2" />
					<ellipse cx="120" cy="184" rx="31" ry="32" fill="#d5b18c" />
					<circle cx="76" cy="78" r="17" fill="#bc936e" stroke="#a97d58" stroke-width="2" />
					<circle cx="160" cy="78" r="17" fill="#bc936e" stroke="#a97d58" stroke-width="2" />
					<circle cx="76" cy="78" r="7" fill="#9b7558" />
					<circle cx="160" cy="78" r="7" fill="#9b7558" />
					<path d="M51 116q0-42 45-42h48q45 0 45 43l2 20q0 31-39 34H88q-39-3-39-34z" fill="#bc936e"
						stroke="#a97d58" stroke-width="2" />
					<ellipse cx="94" cy="119" rx="3.5" ry="5" fill="#514537" />
					<ellipse cx="147" cy="119" rx="3.5" ry="5" fill="#514537" />
					<ellipse cx="120" cy="141" rx="20" ry="13" fill="#d1ab85" />
					<path d="M113 137v4m14-4v4m-16 7q9 6 18 0" stroke="#70513c" stroke-width="2"
						stroke-linecap="round" />
					<path d="M80 185l4 18m76-18-4 18" stroke="#a97d58" stroke-width="3" stroke-linecap="round" />
					<circle cx="120" cy="63" r="15" fill="#efad4c" />
					<path d="M119 48q9-13 17-5-6 9-17 5" fill="#728650" />
					<!-- 小地圖 -->
					<path d="M158 151l25-7 23 8v39l-23-8-25 7z" fill="#fff8e8" stroke="#9b896b" stroke-width="2"
						stroke-linejoin="round" />
					<path d="m164 159 12-4 7 4 14-4m-33 16 12-4 7 4 14-4" fill="none" stroke="#9aaa83" stroke-width="2"
						stroke-linecap="round" />
					<path d="m184 150 5 7-5 7" fill="none" stroke="#d99780" stroke-width="2" />
				</svg>
				<!-- 糯米兔 -->
				<svg class="animal bunny" viewBox="0 0 180 210" role="img" aria-label="糯米兔">
					<ellipse cx="90" cy="191" rx="53" ry="8" fill="#657052" opacity=".13" />
					<path d="M42 119q0-36 48-36t48 36v47q0 19-19 19H61q-19 0-19-19z" fill="#fff9ec" stroke="#ded6c2"
						stroke-width="2" />
					<ellipse cx="90" cy="164" rx="25" ry="27" fill="#fff2d9" />
					<ellipse cx="65" cy="44" rx="14" ry="43" transform="rotate(-10 65 44)" fill="#fff9ec"
						stroke="#ded6c2" stroke-width="2" />
					<ellipse cx="113" cy="42" rx="13" ry="42" transform="rotate(9 113 42)" fill="#fff9ec"
						stroke="#ded6c2" stroke-width="2" />
					<ellipse cx="65" cy="44" rx="6" ry="28" transform="rotate(-10 65 44)" fill="#ecc1b3" />
					<ellipse cx="113" cy="42" rx="5" ry="27" transform="rotate(9 113 42)" fill="#ecc1b3" />
					<path d="M32 111q0-39 58-39t58 39l2 16q0 32-60 32t-60-32z" fill="#fff9ec" stroke="#ded6c2"
						stroke-width="2" />
					<ellipse cx="61" cy="132" rx="9" ry="4" fill="#e79b91" opacity=".65" />
					<ellipse cx="119" cy="132" rx="9" ry="4" fill="#e79b91" opacity=".65" />
					<ellipse cx="70" cy="115" rx="3" ry="4.5" fill="#514537" />
					<ellipse cx="110" cy="115" rx="3" ry="4.5" fill="#514537" />
					<path d="m86 126 4-3 4 3-4 4z" fill="#a16e61" />
					<path d="M90 130q0 7-6 5m6-5q0 7 6 5" fill="none" stroke="#816754" stroke-width="1.7"
						stroke-linecap="round" />
					<path d="M67 174l5 16m41-16-5 16" stroke="#ded6c2" stroke-width="3" stroke-linecap="round" />
					<path d="M83 166l12 24 11-27" fill="#ed9a5c" />
					<path d="m96 168-8-10m12 10 8-11" stroke="#82945b" stroke-width="5" stroke-linecap="round" />
				</svg>
				<div class="speech">阿慢說：<b>別急，我們找找 ♡</b></div>
				<span class="ground-note">TAKE A BREATH · YOU ARE SAFE HERE</span>
			</section>
		</main>

		<footer><span class="paw">✿</span> 毛茸茸小日子 <span>·</span> 一個可以安心放空的小角落。</footer>
	</div>
</template>