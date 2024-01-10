<script>
	import Carousel from 'svelte-carousel';
	import { browser } from '$app/environment';
	import { blur } from 'svelte/transition';

	let carousel; // for calling methods of the carousel instance

	const handleNextClick = () => {
		carousel.goToNext();
	};

	const handlePrevClick = () => {
		carousel.goToPrev();
	};

	let showCardId = 0;

	let isModalOpen = false;

	function openModal() {
		isModalOpen = true;
	}

	function closeModal() {
		isModalOpen = false;
	}
</script>

<div class="relative">
	<div class="md:absolute md:top-[14rem] left-16 mt-4 sm:ml-10 ml-6">
		<h1 class="text-white font-black text-6xl leading-[1.16]">
			WELCOME TO <br /> JITSIE IITM <br /> SOCIETY
		</h1>
		<h2 class="text-white mt-4 text-lg sm:text-xl">
			We Incubate...., We Ignite....., We Innovate.....
		</h2>
		<div class="mt-12">
			<button class="text-white bg-[#3B54C5] px-6 py-4 rounded-xl font-bold">Contact Us</button>
			<a
				href="https://forms.gle/ead7AyeCpLN3GKeX8"
				class="underline text-white ml-5 font-bold decoration-slate-400 underline-offset-4"
				>Join Us</a
			>
		</div>
	</div>

	<div class="md:absolute md:right-0 md:top-5 sm:mt-0 mt-16">
		<svg
			xmlns="http://www.w3.org/2000/svg"
			class="md:w-[850px] md:h-[591px] scale-120 sm:scale-100"
			viewBox="0 0 803 591"
			fill="none"
		>
			<path
				d="M1276.62 590.5C1377.33 590.5 1461.64 504.571 1414.78 415.423C1385.61 359.916 1342.85 309.482 1288.95 266.999C1235.04 224.516 1171.05 190.817 1100.62 167.826C1030.19 144.834 954.705 133 878.472 133C802.24 133 875.43 -20.4914 805 2.5001C743.177 22.6822 461.952 204.319 357.686 277.142C335.947 292.326 313.289 308.005 286.776 307.566C242.028 306.826 178.719 288.299 129.573 282.946C78.9085 277.427 43.4203 312.511 19.624 357.578C-41.7788 473.867 53.6053 590.5 185.11 590.5H878.472H1276.62Z"
				fill="url(#paint0_linear_113_666)"
			/>
			<defs>
				<linearGradient
					id="paint0_linear_113_666"
					x1="741.472"
					y1="133"
					x2="741.472"
					y2="1048"
					gradientUnits="userSpaceOnUse"
				>
					<stop stop-color="#D9D9D9" />
					<stop offset="0.890625" stop-color="#EFCCCC" stop-opacity="0.864583" />
					<stop offset="1" stop-color="#D9D9D9" stop-opacity="0" />
				</linearGradient>
			</defs>
		</svg>
	</div>
	<div class="absolute right-0 sm:right-10 md:top-4 sm:top-[17rem] top-[20rem]">
		<img
			src="/img/jt.webp"
			alt=""
			class="sm:h-[37rem] h-[24rem] object-contain"
			style="-webkit-transform: scaleX(1);
        transform: scaleX(1);"
		/>
	</div>
</div>
<br />
<div class="md:mt-[40rem] mt-20">
	<div class="w-full">
		<div class="bg-[#40484C] w-fit mx-auto flex flex-row rounded-2xl py-5">
			<div class="text-center text-white sm:w-40 w-32">
				<p class="font-bold text-5xl">49</p>
				<p class="mt-3">Pre Incubation</p>
			</div>
			<div class="text-center border-l-4 border-white sm:w-40 w-32 text-white">
				<p class="font-bold text-5xl">19</p>
				<p class="mt-3">Partners</p>
			</div>
			<div class="text-center border-l-4 border-white sm:w-40 w-32 text-white">
				<p class="font-bold text-5xl">60+</p>
				<p class="mt-3">Startups</p>
			</div>
		</div>
	</div>

	<div class="text-center mt-32">
		<h1 class="text-white text-5xl font-bold">JITSIE</h1>
		<br />
		<p class="text-neutral-300 text-2xl">Where creativity meets valuable opportunities</p>
	</div>

	<div class="md:px-16 sm:px-8 px-6">
		<div class="grid sm:grid-cols-2 gap-8 md:flex md:flex-row mt-16">
			<button
				on:click={() => (showCardId = 0)}
				id="defaultBtnClicked"
				class={'text-white text-center w-full pb-3 text-lg ' +
					[showCardId == 0 ? 'text-[#3B54C5] border-b-2 border-[#3B54C5]' : '']}
				>WEN Think Startup Series
			</button>
			<button
				on:click={() => (showCardId = 1)}
				class={'text-white text-center w-full pb-3 text-lg ' +
					[showCardId == 1 ? 'text-[#3B54C5] border-b-2 border-[#3B54C5]' : '']}
				>Start-A-Thon</button
			>
			<button
				on:click={() => (showCardId = 2)}
				class={'text-white text-center w-full pb-3 text-lg ' +
					[showCardId == 2 ? 'text-[#3B54C5] border-b-2 border-[#3B54C5]' : '']}
				>Building Startups using ChatGPT</button
			>
		</div>

		{#if showCardId == 0}
			<div in:blur={{ amount: 10 }}>
				<div class="md:flex mt-16 sm:w-[85%] mx-auto">
					<img src="img/startupseries.png" alt="" class="w-[30rem] h-96 rounded-2xl object-cover" />
					<div class="mt-12 md:ml-20 md:w-[50%]">
						<h1 class="text-white text-3xl font-bold">WEN Think Startup Series</h1>
						<br />
						<p class="text-neutral-300">
							Wadhwani Entrepreneur Network (WEN) Think Startup serves as the inaugural phase in the
							WEN series, aiming to guide students in identifying meaningful problems, validating
							their ideas, and preparing for effective pitching. This online workshop series, led by
							distinguished startup mentors and angel investors Mr Ajay Batra, Mr Pratapaditya
							Chakravarty, Mr Chandan Kar, and Mrs Aarti, offers a comprehensive and experiential
							program. It assists students in generating and validating startup ideas,
							systematically transforming them into a minimum viable product (MVP).
						</p>
						<br />
						<br />
						<a
							on:click={openModal}
							href="#"
							class="text-white underline underline-offset-8 font-bold decoration-[#3B54C5]"
						>
							Learn More
						</a>
					</div>
					<div />
				</div>
			</div>
		{/if}

		{#if showCardId == 1}
			<div in:blur={{ amount: 10 }}>
				<div class="md:flex mt-16 sm:w-[85%] mx-auto">
					<img src="img/startathon.png" alt="" class="w-[30rem] h-96 rounded-2xl object-cover" />
					<div class="mt-12 md:ml-20 md:w-[50%]">
						<h1 class="text-white text-3xl font-bold">Start-A-Thon</h1>
						<br />
						<p class="text-neutral-300">
							START-A-THON was an epic fusion of the adrenaline-pumping intensity of a 48-hour
							hackathon and the thrill of 'Shark Tank' pitching to angel investors. The event's
							motto, "Come with Ideas, Leave with Funded Startups," encapsulated the spirit of what
							unfolded during this groundbreaking initiative.
						</p>
						<br />
						<br />
						<a
							on:click={openModal}
							href="#"
							class="text-white underline underline-offset-8 font-bold decoration-[#3B54C5]"
						>
							Learn More
						</a>
					</div>
					<div />
				</div>
			</div>
		{/if}

		{#if showCardId == 2}
			<div in:blur={{ amount: 10 }}>
				<div class="md:flex mt-16 sm:w-[85%] mx-auto">
					<img src="img/chatgpt.png" class="w-[30rem] h-96 rounded-2xl object-cover" />
					<div class="mt-12 md:ml-20 md:w-[50%]">
						<h1 class="text-white text-3xl font-bold">Building Startups using ChatGPT</h1>
						<br />
						<p class="text-neutral-300">
							To empower young minds on their entrepreneurial journey, we gave out a course,
							"Introduction to Building Startups using ChatGPT," led by Mr Ajay Batra, an Angel
							Investor and the Founding CEO of Unicorn Growth Ventures, exclusively for JITSIE
							members. Originally priced at INR 799, this course was provided for free, garnering
							enthusiasm from 700+ JITSIANs who promptly enrolled.
						</p>
						<br />
						<br />
						<a
							on:click={openModal}
							href="#"
							class="text-white underline underline-offset-8 font-bold decoration-[#3B54C5]"
						>
							Learn More
						</a>
					</div>
					<div />
				</div>
			</div>
		{/if}
		{#if showCardId == 3}
			<div in:blur={{ amount: 10 }}>
				<div class="md:flex mt-16 sm:w-[85%] mx-auto">
					<img
						src="https://hips.hearstapps.com/hmg-prod/images/gettyimages-1229892983-square.jpg?crop=1.00xw:1.00xh;0,0&resize=1200:*"
						alt=""
						class="w-[30rem] h-96 rounded-2xl object-cover"
					/>
					<div class="mt-12 md:ml-20 md:w-[50%]">
						<h1 class="text-white text-3xl font-bold">Open Source + Movie Night</h1>
						<br />
						<p class="text-neutral-300">
							We engaged in skill-building recreational activities that blend learning and leisure
							with our open-source coding sessions and movie nights. It helped participants enhance
							their skills and unwind with an entertaining film, our skill-building recreational
							events offer a dynamic combination of educational and leisurely pursuits. It was a
							blend of knowledge and entertainment, fostering a community where skill development is
							both enriching and enjoyable.
						</p>
						<br />
						<br />
						<a
							on:click={openModal}
							href="#"
							class="text-white underline underline-offset-8 font-bold decoration-[#3B54C5]"
						>
							Learn More
						</a>
					</div>
					<div />
				</div>
			</div>
		{/if}

		<div>
			<div class="text-center mt-32 pb-12 border-neutral-500 border-b-2">
				<h1 class="text-white text-5xl font-bold">About JITSIE</h1>
				<br />
				<p class="text-neutral-300">
					Where Creativity Meets Valuable Opportunities!<br />Where Your Entrepreneurial Dreams Come
					To Life!!
				</p>
			</div>

			<div class="grid md:grid-cols-2 gap-12 mt-16">
				<div>
					<h1 class="text-white text-2xl">Empowering Entrepreneurs Across Diverse Frontiers</h1>
					<p class="text-neutral-400 mt-2">
						Welcome to JITSIE, where your entrepreneurial dreams come to life! Our main aim is to
						support budding entrepreneurs to convert aspirations into reality. JITSIE has already
						grown into a community of 1000+ aspiring entrepreneurs spanning diverse fields such as
						edtech, fintech, consulting, ERP, SaaS, sustainability, space research, pharma-tech,
						biotechnology, tourism and food-tech.
					</p>

					<img src="img/first.JPG" class="h-96 w-full object-cover rounded-2xl mt-4" alt="" />
				</div>
				<div>
					<h1 class="text-white text-2xl">
						Stellar Partnerships and Cosmic Impact in Deep-Tech Startups
					</h1>
					<p class="text-neutral-400 mt-2">
						Our community has garnered the support of influential partners such as the Wadhwani
						Foundation, Startup Ignition Cell, RVEI, and Karo Startup, to name a few. At JITSIE, we
						believe in promoting a deep-tech startup culture that will have a cosmic impact on the
						startup ecosystem. We invite you to join us and start your entrepreneurial journey with
						the support of a thriving community. Let's turn your aspirations into reality!
					</p>
					<img src="img/second.JPG" class="h-96 w-full object-cover rounded-2xl mt-4" alt="" />
				</div>
			</div>

			<div class="grid sm:grid-cols-2 md:grid-cols-4 mt-16 gap-8">
				<div>
					<img src="img/one.png" class="h-60 w-70 object-cover rounded-2xl mt-4 pl-9" alt="" />
					<h1 class="text-white text-xl">Diverse Engagement Initiatives</h1>
					<p class="text-neutral-400 mt-1.5">
						JITSIE fosters entrepreneurship awareness with startup cohorts, startathons, and
						innovation conclaves, fostering a dynamic creating a vibrant community.
					</p>
				</div>
				<div>
					<img src="img/two.png" class="h-60 w-70 object-cover rounded-2xl mt-4 pl-9" alt="" />
					<h1 class="text-white text-xl">Educational Empowerment</h1>
					<p class="text-neutral-400 mt-1.5">
						We hosted events like START-A-THON, offered free courses like ‘Building Startups using
						ChatGPT’ and launched the 'Wadhwani Startup Cohort, fostering innovation and growth
					</p>
				</div>
				<div>
					<img src="img/three.png" class="h-60 w-70 object-cover rounded-2xl mt-4 pl-9" alt="" />
					<h1 class="text-white text-xl">Incubation and Research & Development (R&D)</h1>
					<p class="text-neutral-400 mt-1.5">
						JITSIE nurtures comprehensive incubation, R&D, and strategic connections with angel
						investors and venture capitalists for holistic growth and success.
					</p>
				</div>
				<div>
					<img src="img/four.png" class="h-60 w-70 rounded-2xl mt-4 pl-9" alt="" />
					<h1 class="text-white text-xl">Leadership and Mentorship</h1>
					<p class="text-neutral-400 mt-1.5">
						Experienced leaders, including Kriti Soni and Chandan Kar, guide 'Idea Pitching and 1:1
						Mentorship' sessions, propelling successful idea implementation and growth.
					</p>
				</div>
			</div>
		</div>
	</div>
</div>
{#if isModalOpen}
	<div class="modal">
		<div class="modal-content">
			<p>Under Development</p>
			<button on:click={closeModal}>Close</button>
		</div>
	</div>
{/if}

<style>
	/* Add your modal styles here */
	.modal {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background: rgba(0, 0, 0, 0.5);
		display: flex;
		justify-content: center;
		align-items: center;
		z-index: 999;
	}

	.modal-content {
		background: white;
		padding: 20px;
		border: 1px solid #ccc;
		box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
		text-align: center;
	}
</style>
