Calendar
===
[![](https://jitpack.io/v/quanghd96/AndroidCalendar.svg)](https://jitpack.io/#quanghd96/AndroidCalendar)

Instructions：
---
* Use of MonthCalendarView<br/>
```
<com.jeek.calendar.widget.calendar.month.MonthCalendarView
    android:id="@+id/mcvCalendar"
    android:layout_width="match_parent"
    android:layout_height="@dimen/small_month_calendar_height"
    app:month_day_text_size="@integer/small_calendar_text_size"
    app:month_selected_circle_color="@color/color_select_date_dialog_edit_text_bg_focus"
    app:month_selected_circle_today_color="@color/color_select_date_dialog_edit_text_bg_focus"
    app:month_show_lunar="true"
    app:month_show_task_hint="false"
    app:month_show_holiday_hint="true"
    app:month_text_size="@integer/small_calendar_text_size"/>
```

* Use of ScheduleLayout<br/>

The layout_schedule.xml file must contain MonthCalendarView, WeekCalendarView, and ScheduleRecyclerView. You can directly reference the modified file as a layout.<br/>

```
ScheduleLayout：
app:default_view="week" <!-Default week view->
app:default_view="month" <!-Default month view->
app:auto_change_month_row="false" <!-Does not automatically change five or six lines->
app:auto_change_month_row="true" <!-Automatically change five or six lines->
```

* Set date listener<br/>
```
slSchedule.setOnCalendarClickListener(new OnCalendarClickListener() {
    @Override
    public void onClickDate(int year, int month, int day) {
        //Monitor the date of the click
    }
});
```
* Jump to today<br/>
```
slSchedule.getMonthCalendar().setTodayToView();
```
* Jump to a certain day<br/>
```
slSchedule.initData(year, month, day);
```

Install:<br/>
---
```
maven { url 'https://jitpack.io' }
```

```
implementation 'com.github.quanghd96.AndroidCalendar:calendar:1.0'
```

Screenshot:<br/>
---
![image](https://github.com/xiaojianglaile/Calendar/blob/master/raw/jeek_image_1.gif)
![image](https://github.com/xiaojianglaile/Calendar/blob/master/raw/jeek_image_2.png)

License
-------
BSD, part MIT and Apache 2.0. See the [LICENSE][1] file for details.

[1]: https://github.com/quanghd96/AndroidCalendar/blob/master/LICENSE