<script lang="ts">
	const projects = [
		{
			title: 'Deborah Bell Interiors',
			description:
				'A portfolio website for an interior design firm built with React, TypeScript, and Sanity CMS. The site showcases completed interior design projects through an image-rich gallery, allowing the client to independently manage and update their project portfolio through Sanity Studio. Built as a client project to serve as a professional digital showcase for attracting new clients.',
			tech: ['NextJS', 'TypeScript', 'Tailwind CSS', 'Sanity CMS'],
			github: null,
			live: 'https://deborahbellinteriors.com',
			year: '2025'
		},
		{
			title: 'Workout App Backend',
			description:
				'A Go/Fiber backend API for fitness tracking that lets users create custom workouts, log exercises, and track their daily macronutrients - combining workout management and nutrition monitoring in one platform.',
			tech: ['Golang', 'Docker'],
			github: 'https://github.com/ZondaF12/workout-app-backend',
			year: '2025'
		},
		{
			title: 'My Pocket Garage',
			description:
				"My Pocket Garage lets you instantly check any UK vehicle's MOT history, road tax details, and current status by simply entering a number plate. Set custom reminders for MOT, tax, and insurance renewal dates so you never miss an important deadline.",
			tech: ['ReactNative', 'Typescript', 'Tailwind CSS', 'Firebase'],
			github: 'https://github.com/ZondaF12/Car-App',
			live: 'https://apps.apple.com/gb/app/my-pocket-garage/id6447470205',
			year: '2023'
		}
	];
</script>

<div class="min-h-screen bg-zinc-900 font-inter text-zinc-100">
	<div class="mx-auto max-w-4xl px-6 py-16">
		<!-- Header -->
		<div class="mb-12">
			<a href="/" class="mb-6 inline-block text-sm text-zinc-400 transition hover:text-zinc-300">
				← Back to home
			</a>
			<h1 class="text-4xl font-bold">Projects</h1>
			<p class="mt-2 text-zinc-400">Things I've built along the way</p>
		</div>

		<!-- Projects Grid -->
		<div class="space-y-8">
			{#each projects as project}
				<div
					class="group rounded-lg border border-zinc-800 bg-zinc-900/50 p-6 transition hover:border-zinc-700"
				>
					<div class="mb-3 flex items-start justify-between">
						<div>
							<h2 class="text-xl font-semibold text-zinc-100">{project.title}</h2>
							<p class="text-sm text-zinc-500">{project.year}</p>
						</div>
						<div class="flex gap-3">
							{#if project.github}
								<a
									href={project.github}
									target="_blank"
									rel="noopener noreferrer"
									class="text-zinc-400 transition hover:text-zinc-300"
									aria-label="View on GitHub"
								>
									<svg class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
										<path
											fill-rule="evenodd"
											d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"
											clip-rule="evenodd"
										/>
									</svg>
								</a>
							{/if}
							{#if project.live}
								<a
									href={project.live}
									target="_blank"
									rel="noopener noreferrer"
									class="text-zinc-400 transition hover:text-zinc-300"
									aria-label="View live demo"
								>
									<svg
										class="h-5 w-5"
										fill="none"
										stroke="currentColor"
										viewBox="0 0 24 24"
										aria-hidden="true"
									>
										<path
											stroke-linecap="round"
											stroke-linejoin="round"
											stroke-width="2"
											d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"
										/>
									</svg>
								</a>
							{/if}
						</div>
					</div>

					<p class="mb-4 text-zinc-300">{project.description}</p>

					<div class="flex flex-wrap gap-2">
						{#each project.tech as tech}
							<span class="rounded-full bg-zinc-800 px-3 py-1 text-xs text-zinc-300">
								{tech}
							</span>
						{/each}
					</div>
				</div>
			{/each}
		</div>

		<!-- Footer -->
		<div class="mt-16 border-t border-zinc-800 pt-8 text-center">
			<p class="text-zinc-400">
				You can see many more projects on my
				<a
					href="https://github.com/zondaf12"
					target="_blank"
					rel="noopener noreferrer"
					class="text-zinc-100 underline decoration-zinc-600 underline-offset-2 transition hover:decoration-zinc-400"
				>
					GitHub
				</a>
			</p>
		</div>
	</div>
</div>
