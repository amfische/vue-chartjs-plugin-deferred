<script>
	import { Bar } from 'vue-chartjs'
	import deferred from 'chartjs-plugin-deferred'

	export default {
		extends: Bar,
		props: ['chartData', 'options'],
		mounted() {
			this.addPlugin(deferred)
			this.renderChart(this.chartData, this.options)
		}
	}
	
</script>