<script>
	import ViewSelector from '$lib/components/ViewSelector.svelte';
	import ViewSelectorMenu from '$lib/components/ViewSelectorMenu.svelte';
</script>

<div class="w-full flex h-full flex-col">
	<header
		class="relative z-20 flex flex-none items-center justify-between border-b border-gray-200 py-4 px-6"
	>
		<h1 class="text-lg font-semibold text-gray-900">
			<time datetime="2022-01">January 2022</time>
		</h1>
		<div class="flex items-center">
			<div class="flex items-center rounded-md shadow-sm md:items-stretch">
				<button
					type="button"
					class="flex items-center justify-center rounded-l-md border border-r-0 border-gray-300 bg-white py-2 pl-3 pr-4 text-gray-400 hover:text-gray-500 focus:relative md:w-9 md:px-2 md:hover:bg-gray-50"
				>
					<span class="sr-only">Previous month</span>
					<!-- Heroicon name: solid/chevron-left -->
					<svg
						class="h-5 w-5"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
						fill="currentColor"
						aria-hidden="true"
					>
						<path
							fill-rule="evenodd"
							d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z"
							clip-rule="evenodd"
						/>
					</svg>
				</button>
				<button
					type="button"
					class="hidden border-t border-b border-gray-300 bg-white px-3.5 text-sm font-medium text-gray-700 hover:bg-gray-50 hover:text-gray-900 focus:relative md:block"
					>Today</button
				>
				<span class="relative -mx-px h-5 w-px bg-gray-300 md:hidden" />
				<button
					type="button"
					class="flex items-center justify-center rounded-r-md border border-l-0 border-gray-300 bg-white py-2 pl-4 pr-3 text-gray-400 hover:text-gray-500 focus:relative md:w-9 md:px-2 md:hover:bg-gray-50"
				>
					<span class="sr-only">Next month</span>
					<!-- Heroicon name: solid/chevron-right -->
					<svg
						class="h-5 w-5"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
						fill="currentColor"
						aria-hidden="true"
					>
						<path
							fill-rule="evenodd"
							d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
							clip-rule="evenodd"
						/>
					</svg>
				</button>
			</div>
			<div class="hidden md:ml-4 md:flex md:items-center">
				<div class="relative">
					<ViewSelector />

					<!--
            Dropdown menu, show/hide based on menu state.

            Entering: "transition ease-out duration-100"
              From: "transform opacity-0 scale-95"
              To: "transform opacity-100 scale-100"
            Leaving: "transition ease-in duration-75"
              From: "transform opacity-100 scale-100"
              To: "transform opacity-0 scale-95"
          -->
					<ViewSelectorMenu />
				</div>
				<div class="ml-6 h-6 w-px bg-gray-300" />
				<button
					type="button"
					class="focus:outline-none ml-6 rounded-md border border-transparent bg-indigo-600 py-2 px-4 text-sm font-medium text-white shadow-sm hover:bg-indigo-700 focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2"
					>Add event</button
				>
			</div>
			<div class="relative ml-6 md:hidden">
				<button
					type="button"
					class="-mx-2 flex items-center rounded-full border border-transparent p-2 text-gray-400 hover:text-gray-500"
					id="menu-0-button"
					aria-expanded="false"
					aria-haspopup="true"
				>
					<span class="sr-only">Open menu</span>
					<!-- Heroicon name: solid/dots-horizontal -->
					<svg
						class="h-5 w-5"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
						fill="currentColor"
						aria-hidden="true"
					>
						<path
							d="M6 10a2 2 0 11-4 0 2 2 0 014 0zM12 10a2 2 0 11-4 0 2 2 0 014 0zM16 12a2 2 0 100-4 2 2 0 000 4z"
						/>
					</svg>
				</button>

				<!--
          Dropdown menu, show/hide based on menu state.

          Entering: "transition ease-out duration-100"
            From: "transform opacity-0 scale-95"
            To: "transform opacity-100 scale-100"
          Leaving: "transition ease-in duration-75"
            From: "transform opacity-100 scale-100"
            To: "transform opacity-0 scale-95"
        -->
				<div
					class="focus:outline-none absolute right-0 mt-3 w-36 origin-top-right divide-y divide-gray-100 overflow-hidden rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5"
					role="menu"
					aria-orientation="vertical"
					aria-labelledby="menu-0-button"
					tabindex="-1"
				>
					<div class="py-1" role="none">
						<!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
						<a
							href="#"
							class="text-gray-700 block px-4 py-2 text-sm"
							role="menuitem"
							tabindex="-1"
							id="menu-0-item-0">Create event</a
						>
					</div>
					<div class="py-1" role="none">
						<a
							href="#"
							class="text-gray-700 block px-4 py-2 text-sm"
							role="menuitem"
							tabindex="-1"
							id="menu-0-item-1">Go to today</a
						>
					</div>
					<div class="py-1" role="none">
						<a
							href="#"
							class="text-gray-700 block px-4 py-2 text-sm"
							role="menuitem"
							tabindex="-1"
							id="menu-0-item-2">Day view</a
						>
						<a
							href="#"
							class="text-gray-700 block px-4 py-2 text-sm"
							role="menuitem"
							tabindex="-1"
							id="menu-0-item-3">Week view</a
						>
						<a
							href="#"
							class="text-gray-700 block px-4 py-2 text-sm"
							role="menuitem"
							tabindex="-1"
							id="menu-0-item-4">Month view</a
						>
						<a
							href="#"
							class="text-gray-700 block px-4 py-2 text-sm"
							role="menuitem"
							tabindex="-1"
							id="menu-0-item-5">Year view</a
						>
					</div>
				</div>
			</div>
		</div>
	</header>
	<div class="w-full h-full">
		<div class="flex flex-auto flex-col overflow-auto bg-white">
			<div
				style="width: 165%"
				class="flex max-w-full flex-none flex-col sm:max-w-none md:max-w-full"
			>
				<div
					class="sticky top-0 z-10 flex-none bg-white shadow ring-1 ring-black ring-opacity-5 sm:pr-8"
				>
					<div class="grid grid-cols-7 text-sm leading-6 text-gray-500 sm:hidden">
						<button type="button" class="flex flex-col items-center pt-2 pb-3"
							>M <span
								class="mt-1 flex h-8 w-8 items-center justify-center font-semibold text-gray-900"
								>10</span
							></button
						>
						<button type="button" class="flex flex-col items-center pt-2 pb-3"
							>T <span
								class="mt-1 flex h-8 w-8 items-center justify-center font-semibold text-gray-900"
								>11</span
							></button
						>
						<button type="button" class="flex flex-col items-center pt-2 pb-3"
							>W <span
								class="mt-1 flex h-8 w-8 items-center justify-center rounded-full bg-indigo-600 font-semibold text-white"
								>12</span
							></button
						>
						<button type="button" class="flex flex-col items-center pt-2 pb-3"
							>T <span
								class="mt-1 flex h-8 w-8 items-center justify-center font-semibold text-gray-900"
								>13</span
							></button
						>
						<button type="button" class="flex flex-col items-center pt-2 pb-3"
							>F <span
								class="mt-1 flex h-8 w-8 items-center justify-center font-semibold text-gray-900"
								>14</span
							></button
						>
						<button type="button" class="flex flex-col items-center pt-2 pb-3"
							>S <span
								class="mt-1 flex h-8 w-8 items-center justify-center font-semibold text-gray-900"
								>15</span
							></button
						>
						<button type="button" class="flex flex-col items-center pt-2 pb-3"
							>S <span
								class="mt-1 flex h-8 w-8 items-center justify-center font-semibold text-gray-900"
								>16</span
							></button
						>
					</div>

					<div
						class="-mr-px hidden grid-cols-7 divide-x divide-gray-100 border-r border-gray-100 text-sm leading-6 text-gray-500 sm:grid"
					>
						<div class="col-end-1 w-14" />
						<div class="flex items-center justify-center py-3">
							<span
								>Mon <span class="items-center justify-center font-semibold text-gray-900">10</span
								></span
							>
						</div>
						<div class="flex items-center justify-center py-3">
							<span
								>Tue <span class="items-center justify-center font-semibold text-gray-900">11</span
								></span
							>
						</div>
						<div class="flex items-center justify-center py-3">
							<span class="flex items-baseline"
								>Wed <span
									class="ml-1.5 flex h-8 w-8 items-center justify-center rounded-full bg-indigo-600 font-semibold text-white"
									>12</span
								></span
							>
						</div>
						<div class="flex items-center justify-center py-3">
							<span
								>Thu <span class="items-center justify-center font-semibold text-gray-900">13</span
								></span
							>
						</div>
						<div class="flex items-center justify-center py-3">
							<span
								>Fri <span class="items-center justify-center font-semibold text-gray-900">14</span
								></span
							>
						</div>
						<div class="flex items-center justify-center py-3">
							<span
								>Sat <span class="items-center justify-center font-semibold text-gray-900">15</span
								></span
							>
						</div>
						<div class="flex items-center justify-center py-3">
							<span
								>Sun <span class="items-center justify-center font-semibold text-gray-900">16</span
								></span
							>
						</div>
					</div>
				</div>
				<div class="flex flex-auto">
					<div class="sticky left-0 w-14 flex-none bg-white ring-1 ring-gray-100" />
					<div class="grid flex-auto grid-cols-1 grid-rows-1">
						<!-- Horizontal lines -->
						<div
							class="col-start-1 col-end-2 row-start-1 grid divide-y divide-gray-100"
							style="grid-template-rows: repeat(48, minmax(3.5rem, 1fr))"
						>
							<div class="row-end-1 h-7" />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									12AM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									1AM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									2AM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									3AM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									4AM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									5AM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									6AM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									7AM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									8AM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									9AM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									10AM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									11AM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									12PM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									1PM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									2PM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									3PM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									4PM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									5PM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									6PM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									7PM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									8PM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									9PM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									10PM
								</div>
							</div>
							<div />
							<div>
								<div
									class="sticky left-0 -mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400"
								>
									11PM
								</div>
							</div>
							<div />
						</div>

						<!-- Vertical lines -->
						<div
							class="col-start-1 col-end-2 row-start-1 hidden grid-cols-7 grid-rows-1 divide-x divide-gray-100 sm:grid sm:grid-cols-7"
						>
							<div class="col-start-1 row-span-full" />
							<div class="col-start-2 row-span-full" />
							<div class="col-start-3 row-span-full" />
							<div class="col-start-4 row-span-full" />
							<div class="col-start-5 row-span-full" />
							<div class="col-start-6 row-span-full" />
							<div class="col-start-7 row-span-full" />
							<div class="col-start-8 row-span-full w-8" />
						</div>

						<!-- Events -->
						<ol
							class="col-start-1 col-end-2 row-start-1 grid grid-cols-1 sm:grid-cols-7 sm:pr-8"
							style="grid-template-rows: 1.75rem repeat(288, minmax(0, 1fr)) auto"
						>
							<li class="relative mt-px flex sm:col-start-3" style="grid-row: 74 / span 12">
								<a
									href="#"
									class="group absolute inset-1 flex flex-col overflow-y-auto rounded-lg bg-blue-50 p-2 text-xs leading-5 hover:bg-blue-100"
								>
									<p class="order-1 font-semibold text-blue-700">Breakfast</p>
									<p class="text-blue-500 group-hover:text-blue-700">
										<time datetime="2022-01-12T06:00">6:00 AM</time>
									</p>
								</a>
							</li>
							<li class="relative mt-px flex sm:col-start-3" style="grid-row: 92 / span 30">
								<a
									href="#"
									class="group absolute inset-1 flex flex-col overflow-y-auto rounded-lg bg-pink-50 p-2 text-xs leading-5 hover:bg-pink-100"
								>
									<p class="order-1 font-semibold text-pink-700">Flight to Paris</p>
									<p class="text-pink-500 group-hover:text-pink-700">
										<time datetime="2022-01-12T07:30">7:30 AM</time>
									</p>
								</a>
							</li>
							<li
								class="relative mt-px hidden sm:col-start-6 sm:flex"
								style="grid-row: 122 / span 24"
							>
								<a
									href="#"
									class="group absolute inset-1 flex flex-col overflow-y-auto rounded-lg bg-gray-100 p-2 text-xs leading-5 hover:bg-gray-200"
								>
									<p class="order-1 font-semibold text-gray-700">
										Meeting with design team at Disney
									</p>
									<p class="text-gray-500 group-hover:text-gray-700">
										<time datetime="2022-01-15T10:00">10:00 AM</time>
									</p>
								</a>
							</li>
						</ol>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
