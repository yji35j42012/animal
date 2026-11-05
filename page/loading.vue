<style>
/* =================================
       毛茸茸小日子 - Loading Page
    ================================= */

.loading-screen {
	display: none;
}

.has-loader .loading-screen {
	position: fixed;
	inset: 0;
	z-index: 99999;
	display: flex;
	justify-content: center;
	align-items: center;
	overflow: hidden;

	background:
		radial-gradient(circle at 15% 20%, #f5e9d7 0, transparent 30%),
		radial-gradient(circle at 85% 80%, #e7eee2 0, transparent 35%),
		#fbf8f0;

	opacity: 1;
	visibility: visible;
	transition:
		opacity 0.8s ease,
		visibility 0.8s ease;
}

.loading-screen.is-hidden {
	opacity: 0;
	visibility: hidden;
	pointer-events: none;
}

.loading-content {
	position: relative;
	width: min(90%, 420px);
	text-align: center;
	padding: 30px 20px;
}

/* Logo */

.loading-logo {
	display: flex;
	align-items: center;
	justify-content: center;
	gap: 10px;

	color: #75614d;
	font-size: 24px;
	font-weight: 800;
	letter-spacing: 2px;
}

.loading-paw {
	font-size: 27px;
}

/* 小動物 */

.loading-animals {
	display: flex;
	align-items: center;
	justify-content: center;
	gap: 18px;

	margin: 45px auto 35px;
}

.loading-animal {
	display: flex;
	align-items: center;
	justify-content: center;

	width: 88px;
	height: 88px;

	background: #fffdf8;
	border: 2px solid #eadcc9;
	border-radius: 50%;

	font-size: 48px;
	box-shadow: 0 8px 20px rgba(117, 97, 77, 0.08);

	animation: animal-bounce 1.5s ease-in-out infinite;
}

.loading-animal.rabbit {
	animation-delay: 0.2s;
}

.loading-animal.capybara {
	animation-delay: 0.4s;
}

@keyframes animal-bounce {

	0%,
	100% {
		transform: translateY(0) rotate(0deg);
	}

	50% {
		transform: translateY(-13px) rotate(4deg);
	}
}

/* 載入文字 */

.loading-content h2 {
	color: #75614d;
	font-size: 21px;
	font-weight: 700;
	margin: 0 0 12px;
	letter-spacing: 1px;
}

.loading-content p {
	color: #9b8b78;
	font-size: 14px;
	margin-bottom: 30px;
}

.loading-dots {
	display: inline-block;
	animation: dots 1.2s infinite;
}

@keyframes dots {

	0%,
	20% {
		opacity: 0.2;
	}

	50% {
		opacity: 1;
	}

	100% {
		opacity: 0.2;
	}
}

/* 進度條 */

.loading-progress {
	width: 100%;
	height: 12px;

	background: #e9e4d8;
	border-radius: 20px;
	overflow: hidden;
}

.loading-progress-bar {
	width: 0%;
	height: 100%;

	background: linear-gradient(90deg,
			#a9b99b,
			#d6b994);

	border-radius: 20px;
	transition: width 0.3s ease;
}

.loading-percent {
	margin-top: 10px;
	color: #9b8b78;
	font-size: 13px;
	letter-spacing: 1px;
}

/* 裝飾元素 */

.loading-decor {
	position: absolute;
	color: #b5c4a7;
	font-size: 28px;
	animation: decor-float 3s ease-in-out infinite;
}

.decor-one {
	top: 25%;
	left: 3%;
}

.decor-two {
	top: 35%;
	right: 2%;
	color: #d7aa9c;
}

.decor-three {
	bottom: 25%;
	left: 8%;
	color: #d6b994;
}

.decor-four {
	bottom: 30%;
	right: 5%;
	color: #c5b9a7;
}

@keyframes decor-float {

	0%,
	100% {
		transform: translateY(0) rotate(0deg);
	}

	50% {
		transform: translateY(-10px) rotate(12deg);
	}
}

/* 底部文字 */

.loading-footer {
	margin-top: 35px;
	color: #b3a58f;
	font-size: 10px;
	letter-spacing: 3px;
}

/* 手機版 */

@media (max-width: 480px) {
	.loading-logo {
		font-size: 21px;
	}

	.loading-animal {
		width: 72px;
		height: 72px;
		font-size: 39px;
	}

	.loading-content h2 {
		font-size: 18px;
	}

	.loading-animals {
		gap: 12px;
	}
}

/* 減少動態效果設定 */

@media (prefers-reduced-motion: reduce) {

	.loading-animal,
	.loading-decor,
	.loading-dots {
		animation: none;
	}
}
</style>
<template>
	<div class="load loading-screen" id="loadingScreen" role="status" aria-live="polite">
		<div class="loading-content">

			<div class="loading-decor decor-one">✿</div>
			<div class="loading-decor decor-two">♡</div>
			<div class="loading-decor decor-three">✦</div>
			<div class="loading-decor decor-four">☁</div>

			<div class="loading-logo">
				<span class="loading-paw">🐾</span>
				<span>毛茸茸小日子</span>
			</div>

			<div class="loading-animals">
				<div class="loading-animal cat">🐱</div>
				<div class="loading-animal rabbit">🐰</div>
				<div class="loading-animal capybara">🦫</div>
			</div>

			<h2>正在收集可愛的小日子<span class="loading-dots">...</span></h2>
			<p>小夥伴們正在準備迎接你 ♡</p>

			<div class="loading-progress">
				<div class="loading-progress-bar" id="loadingProgress"></div>
			</div>


			<div class="loading-footer">
				✿ TAKE A LITTLE PAUSE ✿
			</div>

		</div>
	</div>
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
			finished: false,
			isLoad: true,
			in: null,
			contacts: null,
			loccc: null
		};
	},
	mounted() {

		navigator.geolocation.getCurrentPosition(
			(position) => {
				const latitude = position.coords.latitude;
				const longitude = position.coords.longitude;
				this.loccc = "緯度：" + latitude + "經度：" + longitude
			},
			(error) => {
				console.error("定位失敗：", error.message);
			},
			{
				enableHighAccuracy: true,
				timeout: 10000,
				maximumAge: 0
			}
		);
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
			if (data.length == 0) {
				console.log('AAA');
				this.seti()
				setTimeout(() => {
					this.$router.push('/animal');
				}, 1000);
			} else {
				this.contacts.forEach(element => {
					if (element.name === this.in.ip) {
						setTimeout(() => {
							this.$router.push('/animal');
						}, 1000);
						return
					} else {
						this.seti();
						setTimeout(() => {
							this.$router.push('/animal');
						}, 1000);
					}
				});
			}


		},
		async seti() {
			try {
				const response_ipwho = await fetch('https://ipwho.is/');
				const data_ipwho = await response_ipwho.json();
				const { error } = await db
					.from('contacts')
					.insert([
						{
							name: this.in.ip,
							phone: this.in.city,
							note: this.in.country,
							v2: data_ipwho,
							v3: response_ipwho,
						}
					]);
			} catch (error) {
				console.error('取得 IP 失敗', error);
			}
		}
	},
};
</script>