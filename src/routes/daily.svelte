<script>
	import ViewSelector from '$lib/components/ViewSelector.svelte';
	import ViewSelectorMenu from '$lib/components/ViewSelectorMenu.svelte';
</script>

<!-- This example requires Tailwind CSS v2.0+ -->
<div class="w-full flex h-full flex-col">
	<header
		class="relative z-20 flex flex-none items-center justify-between border-b border-gray-200 py-4 px-6"
	>
		<div>
			<h1 class="text-lg font-semibold leading-6 text-gray-900">
				<time datetime="2022-01-22" class="sm:hidden">Jan 22, 2022</time>
				<time datetime="2022-01-22" class="hidden sm:inline">January 22, 2022</time>
			</h1>
		</div>
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
	<div class="w-full">
		<div class="flex flex-auto overflow-hidden bg-white">
			<div class="flex flex-auto flex-col overflow-auto">
				<div
					class="sticky top-0 z-10 grid flex-none grid-cols-7 bg-white text-xs text-gray-500 shadow ring-1 ring-black ring-opacity-5 md:hidden"
				>
					<button type="button" class="flex flex-col items-center pt-3 pb-1.5">
						<span>W</span>
						<!-- Default: "text-gray-900", Selected: "bg-gray-900 text-white", Today (Not Selected): "text-indigo-600", Today (Selected): "bg-indigo-600 text-white" -->
						<span
							class="mt-3 flex h-8 w-8 items-center justify-center rounded-full text-base font-semibold text-gray-900"
							>19</span
						>
					</button>
					<button type="button" class="flex flex-col items-center pt-3 pb-1.5">
						<span>T</span>
						<span
							class="mt-3 flex h-8 w-8 items-center justify-center rounded-full text-base font-semibold text-indigo-600"
							>20</span
						>
					</button>
					<button type="button" class="flex flex-col items-center pt-3 pb-1.5">
						<span>F</span>
						<span
							class="mt-3 flex h-8 w-8 items-center justify-center rounded-full text-base font-semibold text-gray-900"
							>21</span
						>
					</button>
					<button type="button" class="flex flex-col items-center pt-3 pb-1.5">
						<span>S</span>
						<span
							class="mt-3 flex h-8 w-8 items-center justify-center rounded-full bg-gray-900 text-base font-semibold text-white"
							>22</span
						>
					</button>
					<button type="button" class="flex flex-col items-center pt-3 pb-1.5">
						<span>S</span>
						<span
							class="mt-3 flex h-8 w-8 items-center justify-center rounded-full text-base font-semibold text-gray-900"
							>23</span
						>
					</button>
					<button type="button" class="flex flex-col items-center pt-3 pb-1.5">
						<span>M</span>
						<span
							class="mt-3 flex h-8 w-8 items-center justify-center rounded-full text-base font-semibold text-gray-900"
							>24</span
						>
					</button>
					<button type="button" class="flex flex-col items-center pt-3 pb-1.5">
						<span>T</span>
						<span
							class="mt-3 flex h-8 w-8 items-center justify-center rounded-full text-base font-semibold text-gray-900"
							>25</span
						>
					</button>
				</div>
				<div class="flex w-full flex-auto">
					<div class="w-14 flex-none bg-white ring-1 ring-gray-100" />
					<div class="grid flex-auto grid-cols-1 grid-rows-1">
						<!-- Horizontal lines -->
						<div
							class="col-start-1 col-end-2 row-start-1 grid divide-y divide-gray-100"
							style="grid-template-rows: repeat(48, minmax(3.5rem, 1fr))"
						>
							<div class="row-end-1 h-7" />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									12AM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									1AM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									2AM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									3AM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									4AM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									5AM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									6AM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									7AM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									8AM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									9AM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									10AM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									11AM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									12PM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									1PM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									2PM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									3PM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									4PM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									5PM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									6PM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									7PM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									8PM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									9PM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									10PM
								</div>
							</div>
							<div />
							<div>
								<div class="-mt-2.5 -ml-14 w-14 pr-2 text-right text-xs leading-5 text-gray-400">
									11PM
								</div>
							</div>
							<div />
						</div>

						<!-- Events -->
						<ol
							class="col-start-1 col-end-2 row-start-1 grid grid-cols-1"
							style="grid-template-rows: 1.75rem repeat(288, minmax(0, 1fr)) auto"
						>
							<li class="relative mt-px flex" style="grid-row: 74 / span 12">
								<a
									href="#"
									class="group absolute inset-1 flex flex-col overflow-y-auto rounded-lg bg-blue-50 p-2 text-xs leading-5 hover:bg-blue-100"
								>
									<p class="order-1 font-semibold text-blue-700">Breakfast</p>
									<p class="text-blue-500 group-hover:text-blue-700">
										<time datetime="2022-01-22T06:00">6:00 AM</time>
									</p>
								</a>
							</li>
							<li class="relative mt-px flex" style="grid-row: 92 / span 30">
								<a
									href="#"
									class="group absolute inset-1 flex flex-col overflow-y-auto rounded-lg bg-pink-50 p-2 text-xs leading-5 hover:bg-pink-100"
								>
									<p class="order-1 font-semibold text-pink-700">Flight to Paris</p>
									<p class="order-1 text-pink-500 group-hover:text-pink-700">
										John F. Kennedy International Airport
									</p>
									<p class="text-pink-500 group-hover:text-pink-700">
										<time datetime="2022-01-22T07:30">7:30 AM</time>
									</p>
								</a>
							</li>
							<li class="relative mt-px flex" style="grid-row: 134 / span 18">
								<a
									href="#"
									class="group absolute inset-1 flex flex-col overflow-y-auto rounded-lg bg-indigo-50 p-2 text-xs leading-5 hover:bg-indigo-100"
								>
									<p class="order-1 font-semibold text-indigo-700">Sightseeing</p>
									<p class="order-1 text-indigo-500 group-hover:text-indigo-700">Eiffel Tower</p>
									<p class="text-indigo-500 group-hover:text-indigo-700">
										<time datetime="2022-01-22T11:00">11:00 AM</time>
									</p>
								</a>
							</li>
						</ol>
					</div>
				</div>
			</div>
			<div class="hidden w-1/2 max-w-md flex-none border-l border-gray-100 py-10 px-8 md:block">
				<div class="flex items-center text-center text-gray-900">
					<button
						type="button"
						class="-m-1.5 flex flex-none items-center justify-center p-1.5 text-gray-400 hover:text-gray-500"
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
					<div class="flex-auto font-semibold">January 2022</div>
					<button
						type="button"
						class="-m-1.5 flex flex-none items-center justify-center p-1.5 text-gray-400 hover:text-gray-500"
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
				<div class="mt-6 grid grid-cols-7 text-center text-xs leading-6 text-gray-500">
					<div>M</div>
					<div>T</div>
					<div>W</div>
					<div>T</div>
					<div>F</div>
					<div>S</div>
					<div>S</div>
				</div>
				<div
					class="isolate mt-2 grid grid-cols-7 gap-px rounded-lg bg-gray-200 text-sm shadow ring-1 ring-gray-200"
				>
					<!--
          Always include: "py-1.5 hover:bg-gray-100 focus:z-10"
          Is current month, include: "bg-white"
          Is not current month, include: "bg-gray-50"
          Is selected or is today, include: "font-semibold"
          Is selected, include: "text-white"
          Is not selected, is not today, and is current month, include: "text-gray-900"
          Is not selected, is not today, and is not current month, include: "text-gray-400"
          Is today and is not selected, include: "text-indigo-600"

          Top left day, include: "rounded-tl-lg"
          Top right day, include: "rounded-tr-lg"
          Bottom left day, include: "rounded-bl-lg"
          Bottom right day, include: "rounded-br-lg"
        -->
					<button
						type="button"
						class="rounded-tl-lg bg-gray-50 py-1.5 text-gray-400 hover:bg-gray-100 focus:z-10"
					>
						<!--
            Always include: "mx-auto flex h-7 w-7 items-center justify-center rounded-full"
            Is selected and is today, include: "bg-indigo-600"
            Is selected and is not today, include: "bg-gray-900"
          -->
						<time
							datetime="2021-12-27"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">27</time
						>
					</button>
					<button
						type="button"
						class="bg-gray-50 py-1.5 text-gray-400 hover:bg-gray-100 focus:z-10"
					>
						<time
							datetime="2021-12-28"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">28</time
						>
					</button>
					<button
						type="button"
						class="bg-gray-50 py-1.5 text-gray-400 hover:bg-gray-100 focus:z-10"
					>
						<time
							datetime="2021-12-29"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">29</time
						>
					</button>
					<button
						type="button"
						class="bg-gray-50 py-1.5 text-gray-400 hover:bg-gray-100 focus:z-10"
					>
						<time
							datetime="2021-12-30"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">30</time
						>
					</button>
					<button
						type="button"
						class="bg-gray-50 py-1.5 text-gray-400 hover:bg-gray-100 focus:z-10"
					>
						<time
							datetime="2021-12-31"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">31</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-01"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">1</time
						>
					</button>
					<button
						type="button"
						class="rounded-tr-lg bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10"
					>
						<time
							datetime="2022-01-02"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">2</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-03"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">3</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-04"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">4</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-05"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">5</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-06"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">6</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-07"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">7</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-08"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">8</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-09"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">9</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-10"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">10</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-11"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">11</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-12"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">12</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-13"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">13</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-14"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">14</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-15"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">15</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-16"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">16</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-17"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">17</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-18"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">18</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-19"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">19</time
						>
					</button>
					<button
						type="button"
						class="bg-white py-1.5 font-semibold text-indigo-600 hover:bg-gray-100 focus:z-10"
					>
						<time
							datetime="2022-01-20"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">20</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-21"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">21</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-22"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full bg-gray-900 font-semibold text-white"
							>22</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-23"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">23</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-24"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">24</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-25"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">25</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-26"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">26</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-27"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">27</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-28"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">28</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-29"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">29</time
						>
					</button>
					<button type="button" class="bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10">
						<time
							datetime="2022-01-30"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">30</time
						>
					</button>
					<button
						type="button"
						class="rounded-bl-lg bg-white py-1.5 text-gray-900 hover:bg-gray-100 focus:z-10"
					>
						<time
							datetime="2022-01-31"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">31</time
						>
					</button>
					<button
						type="button"
						class="bg-gray-50 py-1.5 text-gray-400 hover:bg-gray-100 focus:z-10"
					>
						<time
							datetime="2022-02-01"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">1</time
						>
					</button>
					<button
						type="button"
						class="bg-gray-50 py-1.5 text-gray-400 hover:bg-gray-100 focus:z-10"
					>
						<time
							datetime="2022-02-02"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">2</time
						>
					</button>
					<button
						type="button"
						class="bg-gray-50 py-1.5 text-gray-400 hover:bg-gray-100 focus:z-10"
					>
						<time
							datetime="2022-02-03"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">3</time
						>
					</button>
					<button
						type="button"
						class="bg-gray-50 py-1.5 text-gray-400 hover:bg-gray-100 focus:z-10"
					>
						<time
							datetime="2022-02-04"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">4</time
						>
					</button>
					<button
						type="button"
						class="bg-gray-50 py-1.5 text-gray-400 hover:bg-gray-100 focus:z-10"
					>
						<time
							datetime="2022-02-05"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">5</time
						>
					</button>
					<button
						type="button"
						class="rounded-br-lg bg-gray-50 py-1.5 text-gray-400 hover:bg-gray-100 focus:z-10"
					>
						<time
							datetime="2022-02-06"
							class="mx-auto flex h-7 w-7 items-center justify-center rounded-full">6</time
						>
					</button>
				</div>
			</div>
		</div>
	</div>
</div>
