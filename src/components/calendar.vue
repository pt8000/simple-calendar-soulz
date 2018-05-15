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
					{startDate: '2018-05-16 14:15', endDate: '2018-05-16 15:00', title: 'test evente 1', id: 13634},
					{startDate: '2018-05-16 12:00', endDate: '2018-05-16 12:10', title: 'test evente 1 bis', id: 1367},
					{startDate: '2018-05-14 06:25', endDate: '2018-05-14 08:30', title: 'test evente 2', id: 2234},
					{startDate: '2018-05-15 07:35', endDate: '2018-05-15 09:00', title: 'test evente 3', id: 1243},
					{startDate: '2018-05-16 21:15', endDate: '2018-05-16 22:00', title: 'test evente 4', id: 22234},
					{startDate: '2018-05-17 08:40', endDate: '2018-05-17 13:06', title: 'test evente 5', id: 7656},
					{startDate: '2018-05-19 06:50', endDate: '2018-05-19 09:00', title: 'test evente 6', id: 2345}
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