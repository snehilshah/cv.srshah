<script>
	import Icon from '@iconify/svelte';
	import { userInfo } from '$lib/Constants';

	let projects = [
		{
			name: 'S3A-Net for FSL Based HSI Classification',
			href: 'https://github.com/',
			desc: 'Experimental investigations on benchmark Hyper Spectral Images datasets',
			tool_icons: ['simple-icons:python', 'simple-icons:tensorflow'],
			github: true
		},
		{
			name: 'Plan - IT ©',
			href: 'https://agenda-builder.vercel.app/',
			desc: 'An event planning application facilitating collaborative scheduling across multiple users, featuring intuitive drag-and-drop functionality for scheduling tasks',
			tool_icons: ['akar-icons:nextjs-fill', 'devicon-plain:javascript', 'simple-icons:mongodb'],
			github: false
		},
		{
			name: 'Project Gallery',
			href: 'https://github.com/srshah27/project-gallery',
			desc: 'A open source project to showcase your projects in a beautiful way The Frontend for Github',
			tool_icons: ['akar-icons:nextjs-fill', 'devicon-plain:javascript', 'simple-icons:mongodb'],
			github: true
		},
		{
			name: 'IDF balgurukul',
			href: 'https://idfbalgurukul.com/',
			desc: 'A streamlined student data portal for 300+ Balgurukuls, enhancing efficiency and accuracy.',
			tool_icons: ['akar-icons:nextjs-fill', 'devicon-plain:javascript', 'simple-icons:mongodb'],
			github: false
		},
		{
			name: 'Mini Project in P5*JS',
			href: 'https://adityasawant0912.github.io/P5JS-MiniProjects/',
			desc: 'Numerous mini projects utilizing P5.js, encompassing a diverse array of visualizations and applications.',
			tool_icons: ['simple-icons:p5dotjs'],
			github: true
		},
		{
			name: 'Green Light for Emergency Vehicles',
			href: 'https://www.youtube.com/watch?v=PKuJoiP5wf0',
			desc: 'Implementied a transponder system that communicates with traffic signals to grant priority access. ',
			tool_icons: [],
			github: true
		},
	];
</script>

<svelte:head>
	<title>{userInfo.name}</title>
	<meta
		name="description"
		content="My personal website where you can learn about me, see my resume, and some stuff that I've written"
	/>
	<meta name="og:title" content="Snehil Shah" />
	<meta
		name="og:description"
		content="My personal website wh	ere you can learn about me, see my resume, and some stuff that I've written"
	/>
	<meta name="og:type" content="website" />
	<meta name="og:url" content="https://srshah.me" />
	<meta name="og:site_name" content="srshah.me" />
	<meta name="twitter:title" content="Snehil Shah" />
	<meta
		name="twitter:description"
		content="My personal website where you can learn about me, see my resume, and some stuff that I've written"
	/>
</svelte:head>

<div class="pb-6">
	<h1 class="text-4xl sm:text-5xl my-0">Hi, I'm {userInfo.name} 🦥</h1>
	<p class="text-lg text-neutral-500">{userInfo.description}</p>
</div>

<div class="text-xl space-y-12">
	<div class="space-y-6">
		<p>
			Hey there! I'm deeply passionate about technology and as a dedicated software engineering student at SAKEC, 
			I'm on a mission to make a meaningful impact through my work.
			You are currently looking at my website that <b>my friends</b> built with <b>SvelteKit</b> and 
			<b>TailwindCSS</b>. My expertise lies in <u>web development </u> and <u>software engineering</u>, 
			with a strong command over technologies like <b>Node.js, Next.js, P5.js, PHP, Python, and JavaScript.</b>
		</p>
		<p>
			I serve as <b>Student Co-ordinator</b> at
			<a class="link" href="https://shahandanchor.com/csisakec/">CSI</a>.
		</p>
		<p>
			I'm driven by creativity and technology's endless possibilities. Whether it's crafting elegant code 
			or envisioning groundbreaking research, I'm committed to <u>harnessing technology for positive change and innovation.</u>
		</p>
		<p>
			Working towards that goal, I am currently pursuing a <b>B.E. in Computer Science</b> at
			<a class="link" href="https://www.sakec.ac.in/">Shah & Anchor</a>.
		</p>
		<p>
			I am deeply passionate about the intersection of computer science and artificial intelligence.
			My interests span all the way from front-end development to machine learning, and I thrive on
			solving challenges in algorithms and data structures.
		</p>
		<p>
			And I also like to talk about technolgies I work with sometimes. <br>
			<a
				target="_blank"
				class="link"
				href="https://www.sakec.ac.in/csi-sakec/mastering-the-web/">1. Mastering the Web</a
			>
			<br>
			<a
				target="_blank"
				class="link"
				href="https://www.sakec.ac.in/csi-sakec/level-up-creative-coding-with-p5-js/">2. Level Up: Creative Coding with P5*JS</a
			>
		</p>
	</div>

	<div>
		<h2 class="mb-6">My notable projects:</h2>
		<div class="grid md:grid-cols-3 sm:grid-cols-2 gap-2">
			{#each projects as project}
				<a
					target="_blank"
					href={project.href}
					class="flex flex-col border border-neutral-300 dark:border-neutral-700 dark:bg-neutral-800 justify-between p-6 rounded-lg transition-all shadow-none ease-out duration-150 hover:shadow-3xl hover:dark:bg-[#333333]"
				>
					<div class="flex flex-col gap-y-2">
						<h3 class="font-bold text-xl text-neutral-800 dark:text-neutral-200">
							{project.name}
						</h3>
						<p class="text-base leading-snug text-neutral-600 dark:text-neutral-400">
							{project.desc}
						</p>
					</div>
					<div class="flex flex-row-reverse justify-between">
						{#if project.github}
							<Icon icon="mdi:github" width="18" height="18" class="block mt-4 text-neutral-400" />
						{:else}
							<Icon
								icon="prime:arrow-up-right"
								width="18"
								height="18"
								class="block mt-4 text-neutral-400"
							/>
						{/if}
						<div class="flex gap-2">
							{#each project.tool_icons as icon}
								{#if icon == 'wasm'}
									<div class="block mt-4">
										<svg
											xmlns="http://www.w3.org/2000/svg"
											width="18"
											height="18"
											viewBox="0 0 128 128"
										>
											<path
												fill="#a3a3a3"
												d="M.223.222v127.555h127.555V.222H78.594c.014.227.036.455.036.686c0 8.08-6.55 14.626-14.63 14.626c-8.078 0-14.625-6.546-14.625-14.626c0-.231.022-.459.031-.686zm29.595 68.746h8.445l5.782 30.738h.107l6.968-30.738h7.908l6.265 31.119h.106l6.597-31.119h8.284l-10.765 45.156H61.12l-6.213-30.738H54.8l-6.7 30.738h-8.557zm59.994 0h13.334l13.284 45.156h-8.77l-2.879-10.051H89.59l-2.212 10.05h-8.5ZM94.895 80.1l-3.684 16.57h11.473L98.448 80.1Z"
											/>
										</svg>
									</div>
								{:else}
									<Icon {icon} width="18" height="18" class="block mt-4 text-neutral-400" />
								{/if}
							{/each}
						</div>
					</div>
				</a>
			{/each}
		</div>
	</div>
</div>
