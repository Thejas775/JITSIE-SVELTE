<script>
	let isOpen = false;
</script>

<nav>
	<div class="lg:hidden fixed w-full bg-black h-14 z-[400]">
		<div class="fixed inline-block top-4">
			<button class="relative left-3" on:click={() => (isOpen = !isOpen)}>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="w-7 h-7 {isOpen ? 'hidden' : 'block '}"
					viewBox="0,0,256,256"
				>
					<g
						fill="#3B54C5"
						fill-rule="nonzero"
						stroke="#3B54C5"
						stroke-width="3"
						stroke-linecap="butt"
						stroke-linejoin="miter"
						stroke-miterlimit="10"
						stroke-dasharray=""
						stroke-dashoffset="0"
						font-family="none"
						font-weight="none"
						font-size="none"
						text-anchor="none"
						style="mix-blend-mode: normal"
						><g transform="scale(10.66667,10.66667)"
							><path d="M2,12h20" /><path d="M2,6h20" /><path d="M2,18h20" /><path
								d="M2,12h20"
							/><path d="M22,12h-20" /></g
						></g
					>
				</svg>
				<svg
					fill="#3B54C5"
					class="w-8 h-6 {isOpen ? 'block' : 'hidden'}"
					version="1.1"
					id="Capa_1"
					xmlns="http://www.w3.org/2000/svg"
					xmlns:xlink="http://www.w3.org/1999/xlink"
					viewBox="0 0 94.926 94.926"
					xml:space="preserve"
					><g id="SVGRepo_bgCarrier" stroke-width="0" /><g
						id="SVGRepo_tracerCarrier"
						stroke-linecap="round"
						stroke-linejoin="round"
					/><g id="SVGRepo_iconCarrier">
						<g>
							<path
								d="M55.931,47.463L94.306,9.09c0.826-0.827,0.826-2.167,0-2.994L88.833,0.62C88.436,0.224,87.896,0,87.335,0 c-0.562,0-1.101,0.224-1.498,0.62L47.463,38.994L9.089,0.62c-0.795-0.795-2.202-0.794-2.995,0L0.622,6.096 c-0.827,0.827-0.827,2.167,0,2.994l38.374,38.373L0.622,85.836c-0.827,0.827-0.827,2.167,0,2.994l5.473,5.476 c0.397,0.396,0.936,0.62,1.498,0.62s1.1-0.224,1.497-0.62l38.374-38.374l38.374,38.374c0.397,0.396,0.937,0.62,1.498,0.62 s1.101-0.224,1.498-0.62l5.473-5.476c0.826-0.827,0.826-2.167,0-2.994L55.931,47.463z"
							/>
						</g>
					</g></svg
				>
			</button>
			{#if isOpen}
				<div
					class="absolute left-0 z-20 w-44 py-2 mt-2 origin-top-left bg-slate-800 rounded-md shadow-xl"
				>
					<a
						href="/blogs"
						on:click={() => (isOpen = false)}
						class="block px-6 py-3 text-sm text-white transition-colors duration-300 transform"
					>
						Blogs
					</a>
					<a
						href="#"
						on:click={() => (isOpen = false)}
						class="block px-6 py-3 text-sm text-white transition-colors duration-300 transform"
					>
						Team
					</a>
					<a
						href="#"
						on:click={() => (isOpen = false)}
						class="block px-6 py-3 text-sm text-white transition-colors duration-300 transform"
					>
						Contact
					</a>
					<a
						href="#"
						on:click={() => (isOpen = false)}
						class="block px-6 py-3 text-sm text-white transition-colors duration-300 transform"
					>
						About
					</a>
				</div>
			{/if}
		</div>
		<div class="mx-auto w-fit mt-2">
			<a href="/" class="">
				<img class=" h-12 object-contain" src="/img/image-6@2x.png" alt="" />
			</a>
		</div>

		<div class="fixed right-2 top-4">
			<a
				href="https://forms.gle/ead7AyeCpLN3GKeX8"
				class="py-2 px-4 text-sm text-white bg-[#3B54C5] rounded-xl"
			>
				Join Us
			</a>
		</div>
	</div>

	<div class="hidden lg:block fixed top-0 w-full bg-black h-20 z-[400]">
		<div class="">
			<div class="fixed left-12 top-3">
				<a href="/">
					<img class="h-16 object-contain" src="/img/image-6@2x.png" alt="" />
				</a>
			</div>

			<div class="fixed right-12 top-8">
				<div class="flex flex-row gap-x-14">
					<a href="/blogs" class="text-white hover:underline"> Blogs </a>
					<a href="/team" class="text-white hover:underline"> Team </a>
					<a href="" class=" text-white hover:underline"> Contact </a>
					<a href="" class="text-white hover:underline"> About </a>
					<a href="" class="text-white hover:underline"> Events </a>
					<a
						href="https://forms.gle/ead7AyeCpLN3GKeX8"
						class="py-2 px-6 -mt-1.5 text-sm text-white bg-[#3B54C5] rounded-2xl"
					>
						Join Us
					</a>
				</div>
			</div>
		</div>
	</div>
</nav>
<br />
<br />
<br />
<br />
