<template>
	<div id="cal">
		<h1>My Calendar</h1>
		<calendar-view
			:show-date = "showDate"
			@show-date-change = "setShowDate"			
			:startingDayOfWeek = 1
			:enableDragDrop = true
			displayPeriodUom = "week"
			:events = events
			:showEventTimes = true
			locale = "de"
		/>
	</div>
</template>
<script>
	import CalendarView from "./CalendarView"
	require("../assets/static/css/default.css")
	require("../assets/static/css/holidays-us.css")

	export default {
		data: function() {
			return { 
				showDate: new Date() ,
				events: [
					{startDate: '2018-04-30 06:15', endDate: '2018-04-30 09:00', title: 'test evente 1', id: 13634},
					{startDate: '2018-04-30 07:00', endDate: '2018-04-30 09:00', title: 'test evente 1 bis', id: 1367},
					{startDate: '2018-05-01 06:25', endDate: '2018-05-01 08:30', title: 'test evente 2', id: 2234},
					{startDate: '2018-05-02 07:35', endDate: '2018-05-02 09:00', title: 'test evente 3', id: 1243},
					{startDate: '2018-05-03 07:15', endDate: '2018-05-03 09:00', title: 'test evente 4', id: 22234},
					{startDate: '2018-05-04 08:40', endDate: '2018-05-04 13:06', title: 'test evente 5', id: 7656},
					{startDate: '2018-05-05 06:50', endDate: '2018-05-05 09:00', title: 'test evente 6', id: 2345}
				]
			}
		},
		components: {
			CalendarView
		},
		methods: {
			setShowDate(d) {
				this.showDate = d;
			},
		}
	}
</script>
<style>
	#cal {
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		color: #2c3e50;
		height: 90vh;
		width: 90vw;
		display: flex;
		flex-direction: column;
		margin-left: auto;
		margin-right: auto;
	}
</style>