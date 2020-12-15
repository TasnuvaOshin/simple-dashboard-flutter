# simple-dashboard-flutter
Make Simple Dashboard Using Flutter . 

## Get Started

> Follow the Setup Setps and Easily Make this Dashboard 

- [SETUP](#SETUP)
- [CODE](#CODE)


### SETUP

- Put this Code into pubspec.yaml  file and then Just Sync Your Project Thants it (Or In the terminal write --flutter pub get 
```
 fl_chart: ^0.12.1

```
---

### CODE
```
import 'package:fl_chart/fl_chart.dart';
import 'package:flutter/material.dart';

class DashboardScreen extends StatelessWidget {
  static final dashboardScreenRoute = "/dashboard";
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("Dashboard"),
      ),
      body: Container(
        decoration: BoxDecoration(
            color: Colors.green[100],
            borderRadius: BorderRadius.all(Radius.circular(0))),
        width: double.infinity,
        child: SingleChildScrollView(
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.start,
            children: [
              Padding(
                padding: const EdgeInsets.all(28.0),
                child: RichText(
                  text: TextSpan(
                    text: 'Performance \n',
                    style: TextStyle(fontSize: 18.0, color: Colors.black),
                    children: <TextSpan>[
                      TextSpan(
                          text: 'Analysis',
                          style: TextStyle(
                              fontWeight: FontWeight.w900, fontSize: 22.0)),
                    ],
                  ),
                ),
              ),
              Row(
                mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                children: [
                  SizedBox.fromSize(
                    size: Size(65, 65), // button width and height
                    child: ClipOval(
                      child: Material(
                        elevation: 16.0,
                        color: Colors.orange, // button color
                        child: InkWell(
                          splashColor: Colors.green, // splash color
                          onTap: () {}, // button pressed
                          child: Padding(
                            padding: const EdgeInsets.all(8.0),
                            child: Column(
                              mainAxisAlignment: MainAxisAlignment.center,
                              children: <Widget>[
                                Icon(Icons.date_range,
                                    color: Colors.black54), // icon
                                FittedBox(
                                  child: Text(
                                    "last Month",
                                    style: TextStyle(
                                        color: Colors.black54,
                                        fontWeight: FontWeight.w500),
                                  ),
                                ), // text
                              ],
                            ),
                          ),
                        ),
                      ),
                    ),
                  ),
                  SizedBox.fromSize(
                    size: Size(65, 65), // button width and height
                    child: ClipOval(
                      child: Material(
                        elevation: 16.0,
                        color: Colors.white, // button color
                        child: InkWell(
                          splashColor: Colors.green, // splash color
                          onTap: () {}, // button pressed
                          child: Padding(
                            padding: const EdgeInsets.all(8.0),
                            child: Column(
                              mainAxisAlignment: MainAxisAlignment.center,
                              children: <Widget>[
                                Icon(
                                  Icons.date_range,
                                  color: Colors.black54,
                                ), // icon
                                FittedBox(
                                    child: Text(
                                  "last 3 Month",
                                  style: TextStyle(
                                      color: Colors.black54,
                                      fontWeight: FontWeight.w500),
                                )), // text
                              ],
                            ),
                          ),
                        ),
                      ),
                    ),
                  ),
                  SizedBox.fromSize(
                    size: Size(65, 65), // button width and height
                    child: ClipOval(
                      child: Material(
                        elevation: 16.0,
                        color: Colors.white, // button color
                        child: InkWell(
                          splashColor: Colors.green, // splash color
                          onTap: () {}, // button pressed
                          child: Padding(
                            padding: const EdgeInsets.all(8.0),
                            child: Column(
                              mainAxisAlignment: MainAxisAlignment.center,
                              children: <Widget>[
                                Icon(Icons.date_range,
                                    color: Colors.black54), // icon
                                FittedBox(
                                  child: Text(
                                    "last year",
                                    style: TextStyle(
                                        color: Colors.black54,
                                        fontWeight: FontWeight.w500),
                                  ),
                                ), // text
                              ],
                            ),
                          ),
                        ),
                      ),
                    ),
                  ),
                  SizedBox.fromSize(
                    size: Size(65, 65), // button width and height
                    child: ClipOval(
                      child: Material(
                        elevation: 16.0,
                        color: Colors.white, // button color
                        child: InkWell(
                          splashColor: Colors.green, // splash color
                          onTap: () {}, // button pressed
                          child: Padding(
                            padding: const EdgeInsets.all(8.0),
                            child: Column(
                              mainAxisAlignment: MainAxisAlignment.center,
                              children: <Widget>[
                                Icon(
                                  Icons.date_range,
                                  color: Colors.black54,
                                ), // icon
                                FittedBox(
                                    child: Text(
                                  "All History",
                                  style: TextStyle(
                                      color: Colors.black54,
                                      fontWeight: FontWeight.w500),
                                )), // text
                              ],
                            ),
                          ),
                        ),
                      ),
                    ),
                  ),
                ],
              ),
              Padding(
                padding: const EdgeInsets.all(18.0),
                child: Divider(),
              ),
              Container(
                width: double.infinity,
                child: Padding(
                  padding: const EdgeInsets.only(top: 28.0, right: 18.0),
                  child: BarChart(BarChartData(
                      borderData: FlBorderData(show: false),
                      groupsSpace: 17,
                      barGroups: [
                        BarChartGroupData(
                          x: 1,
                          barRods: [
                            BarChartRodData(
                              y: 4,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.red[900],
                                Colors.red[500],
                                Colors.red,
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                            BarChartRodData(
                              y: 7,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.yellow[900],
                                Colors.yellow[500],
                                Colors.yellow
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                          ],
                        ),
                        BarChartGroupData(
                          x: 2,
                          barRods: [
                            BarChartRodData(
                              y: 2,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.red[900],
                                Colors.red[500],
                                Colors.red,
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                            BarChartRodData(
                              y: 8,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.yellow[900],
                                Colors.yellow[500],
                                Colors.yellow
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                          ],
                        ),
                        BarChartGroupData(
                          x: 3,
                          barRods: [
                            BarChartRodData(
                              y: 1,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.red[900],
                                Colors.red[500],
                                Colors.red,
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                            BarChartRodData(
                              y: 5,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.yellow[900],
                                Colors.yellow[500],
                                Colors.yellow
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                          ],
                        ),
                        BarChartGroupData(
                          x: 4,
                          barRods: [
                            BarChartRodData(
                              y: 6,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.red[900],
                                Colors.red[500],
                                Colors.red,
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                            BarChartRodData(
                              y: 2,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.yellow[900],
                                Colors.yellow[500],
                                Colors.yellow
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                          ],
                        ),
                        BarChartGroupData(
                          x: 5,
                          barRods: [
                            BarChartRodData(
                              y: 2,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.red[900],
                                Colors.red[500],
                                Colors.red,
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                            BarChartRodData(
                              y: 4,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.yellow[900],
                                Colors.yellow[500],
                                Colors.yellow
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                          ],
                        ),
                        BarChartGroupData(
                          x: 6,
                          barRods: [
                            BarChartRodData(
                              y: 8,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.red[900],
                                Colors.red[500],
                                Colors.red,
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                            BarChartRodData(
                              y: 4,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.yellow[900],
                                Colors.yellow[500],
                                Colors.yellow
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                          ],
                        ),
                        BarChartGroupData(
                          x: 7,
                          barRods: [
                            BarChartRodData(
                              y: 2,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.red[900],
                                Colors.red[500],
                                Colors.red,
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                            BarChartRodData(
                              y: 7,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.yellow[900],
                                Colors.yellow[500],
                                Colors.yellow
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                          ],
                        ),
                        BarChartGroupData(
                          x: 8,
                          barRods: [
                            BarChartRodData(
                              y: 12,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.red[900],
                                Colors.red[500],
                                Colors.red,
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                            BarChartRodData(
                              y: 8,
                              width: 8,
                              gradientColorStops: [0.7],
                              colors: [
                                Colors.yellow[900],
                                Colors.yellow[500],
                                Colors.yellow
                              ],
                              borderRadius: BorderRadius.circular(10),
                            ),
                          ],
                        )
                      ])),
                ),
              ),
              Padding(
                padding: const EdgeInsets.all(8.0),
                child: Row(
                  children: [
                    FlatButton.icon(
                      icon:
                          Icon(Icons.invert_colors, color: Colors.yellow[900]),
                      onPressed: () {},
                      label: Text(
                        "Completed Order",
                        style: TextStyle(color: Colors.black54),
                      ),
                    ),
                    FlatButton.icon(
                      icon: Icon(Icons.invert_colors, color: Colors.red),
                      onPressed: () {},
                      label: Text(
                        "Cancelled Order",
                        style: TextStyle(color: Colors.black54),
                      ),
                    ),
                  ],
                ),
              ),
              Padding(
                padding: const EdgeInsets.all(18.0),
                child: Center(
                  child: Column(
                    mainAxisAlignment: MainAxisAlignment.center,
                    crossAxisAlignment: CrossAxisAlignment.center,
                    children: [
                      Padding(
                        padding: const EdgeInsets.all(8.0),
                        child: RichText(
                          text: TextSpan(
                            text: 'Total Completed : ',
                            style:
                                TextStyle(fontSize: 18.0, color: Colors.black),
                            children: <TextSpan>[
                              TextSpan(
                                  text: '129',
                                  style: TextStyle(
                                      fontWeight: FontWeight.w900,
                                      fontSize: 22.0)),
                            ],
                          ),
                        ),
                      ),
                      Padding(
                        padding: const EdgeInsets.all(8.0),
                        child: RichText(
                          text: TextSpan(
                            text: 'Total Cancelled : ',
                            style:
                                TextStyle(fontSize: 18.0, color: Colors.black),
                            children: <TextSpan>[
                              TextSpan(
                                  text: '6',
                                  style: TextStyle(
                                      fontWeight: FontWeight.w900,
                                      fontSize: 22.0)),
                            ],
                          ),
                        ),
                      ),
                    ],
                  ),
                ),
              ),
            ],
          ),
        ),
      ),
    );
  }
}


```
