<template>
	<div class="py-10 container mx-auto">
		<h2 class="text-2xl text-center font-black">FAQ</h2>
		<ul
			class="faq px-8 sm:px-0 grid py-10 grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10"
		>
			<li>
				<label>What is the source ?</label>
				<p>
					Statistics on Mauritius is taken from
					<a target="_blank" href="https://besafemoris.mu/stats/">BeSafeMoris</a
					>, the official news source announced by the Mauritian Government.
					Statistics on all other countries come from
					<a href="https://github.com/CSSEGISandData/COVID-19" target="_blank"
						>John Hopkins CSSE.</a
					>
				</p>
			</li>
			<li>
				<label>What is the difference between Active Cases and Total?</label>
				<p>
					Active cases are the last reported number of people who have the
					infection. It does not include deceased people or people who have
					recovered. Active cases also excludes people who went abroad for treatment.
				</p>
			</li>
			<li>
				<label>Is this page official?</label>
				<p>
					No. This is a community effort to visualize the large flux of data
					coming our way. However all data are taken from official and trusted
					sources i.e BeSafeMoris and John Hopkins CSSE.
				</p>
			</li>
			<li>
				<label>Is the data about Mauritius updated automatically?</label>
				<p>
					Yes. The data is updated every 5 minutes with official data from
					BeSafeMoris.mu. I do keep an independenly maintained copy of the data
					here using
					<a
						target="_blank"
						href="https://docs.google.com/spreadsheets/d/1DhrU8lCWYS_VKKQ3QOYbLzrJgHioQGQp5qPnpSNcUU8/edit?usp=sharing"
						>Google Sheet</a
					>
					just in case the other source fails .
				</p>
			</li>
			<li>
				<label>Is the data about other countries updated automatically?</label>
				<p>
					Yes. The data for other countries is taken from this data source:
					<a target="_blank" href="https://github.com/pomber/covid19/"
						>John Hopkins CSSE data converted to JSON</a
					>
				</p>
			</li>
			<li>
				<label>Why did you build this?</label>
				<p>
					To have a simple page where everyone can check the latest statistics.
				</p>
			</li>
			<li>
				<label
					>Why does this exist when there is an official BeSafeMoris website
					?</label
				>
				<p>
					Please use the official app for faster official updates. On this page
					I will add additional graphic analysis based on the same official data
					showing trends how Mauritius is doing compared to other countries.
				</p>
			</li>
			<li>
				<label>Can COVID-19 ... ?</label>
				<p>
					We hear a lot of measures and information that might slow down or help prevent the spread 
					of COVID-19. Sadly, many of them are incorrect, unproven and/or fake. Please
					refer to the official recommendations from the World Health Organization 
					<a target="_blank" href="https://www.who.int/emergencies/diseases/novel-coronavirus-2019/advice-for-public/myth-busters">
					here</a>.
				</p>
			</li>
			<li>
				<label
					>Are you a journalist or from the Ministry of Health and would you
					like to know more about this page?</label
				>
				<p>
					Get in touch with me asap: san<span class="hidden"></span>dee<span
						class="hidden"
					></span
					>p@ra<span class="hidden"></span>mgo<span class="hidden"></span
					>lam.com
				</p>
			</li>
			<li>
				<label>Can I contribute to this project?</label>
				<p>
					Yes please. This project is open source anyone can submit a PR or
					create an Issue to add new charts or other suggestions
					<a href="https://github.com/MrSunshyne/covid19-mauritius">here</a>.
				</p>
			</li>
		</ul>
	</div>
</template>

<script>
	import {mapGetters} from "vuex";

	export default {
		computed: {
			...mapGetters(["getUpdated"]),
		},
	};
</script>

<style lang="scss" scoped>
	label {
		@apply font-bold my-4;
	}

	a {
		@apply text-blue-600;
	}
</style>
