<script>
	import Icon from '@iconify/svelte';

	let projects = [
		{
			name: 'stock analysis',
			href: 'https://github.com/srshah27/Stock-Analysis',
			desc: 'Stock market technical analysis using python and its libraries to design algorithms for finding the Demand and Supply zone.',
			tool_icons: ['simple-icons:python', 'devicon-plain:pandas-wordmark', 'grommet-icons:mysql'],
			github: true
		},
		{
			name: 'agenda builder',
			href: 'https://agenda-builder.vercel.app/',
			desc: 'An event planning application facilitating collaborative scheduling across multiple users, featuring intuitive drag-and-drop functionality for scheduling tasks',
			tool_icons: ['akar-icons:nextjs-fill', 'devicon-plain:javascript', 'simple-icons:mongodb'],
			github: false
		},
		{
			name: 'IDF balgurukul',
			href: 'https://idfbalgurukul.com/',
			desc: 'A streamlined student data portal for 300+ Balgurukuls, enhancing efficiency and accuracy.',
			tool_icons: ['akar-icons:nextjs-fill', 'devicon-plain:javascript', 'simple-icons:mongodb'],
			github: false
		},
		{
			name: 'srshah.me',
			href: 'https://github.com/srshah27/srshah27',
			desc: 'My personal website built with NextJS and TailwindCSS',
			tool_icons: ['akar-icons:nextjs-fill', 'devicon-plain:javascript', 'simple-icons:mongodb'],
			github: true
		},
		{
			name: 'hyperspectral image',
			href: 'https://github.com/',
			desc: 'Experimental investigations on benchmark Hyper Spectral Images datasets',
			tool_icons: ['simple-icons:python', 'simple-icons:tensorflow'],
			github: true
		},
		{
			name: 'project gallery',
			href: 'https://github.com/srshah27/project-gallery',
			desc: 'A open source project to showcase your projects in a beautiful way The Frontend for Github',
			tool_icons: ['akar-icons:nextjs-fill', 'devicon-plain:javascript', 'simple-icons:mongodb'],
			github: true
		}
	];
</script>

<svelte:head>
	<title>sr.shah</title>
	<meta
		name="description"
		content="My personal website where you can learn about me, see my resume, and some stuff that I've written"
	/>
	<meta name="og:title" content="Snehil Shah" />
	<meta
		name="og:description"
		content="My personal website where you can learn about me, see my resume, and some stuff that I've written"
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
	<h1 class="text-4xl sm:text-5xl my-0">Hi, I'm Aditya 🦥</h1>
	<p class="text-lg text-neutral-500">software engineer, enthusiast, and student</p>
</div>

<div class="text-xl space-y-12">
	<div class="space-y-6">
		<p>
			I do all sorts of programming in my free time. You are currently looking at my website that I
			built with <b>SvelteKit</b> and <b>TailwindCSS</b>. I'm well versed with other programming
			languages such as C++, Java, Python, and Node.
		</p>
		<p>
			I serve as <b>General Co-ordinator</b> at
			<a class="link" href="https://www.shahandanchor.com/">CSI</a>.
		</p>
		<p>
			As a enthusiast, I strive to <b>share knowledge</b> in all that I do, including software
			development. I hope to create <bi>meaningful software</bi> that impacts others in a positive way.
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
			Oh, and, I write blog posts sometimes. Feel free to <a
				target="_blank"
				class="link"
				href="https://srshah.me/blogs">read them</a
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
