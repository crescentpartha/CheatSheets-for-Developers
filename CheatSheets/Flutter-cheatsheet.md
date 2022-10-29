<b>The classic “Hello World” example:</b>

import 'package:flutter/material.dart';

void main() => runApp(HelloWorldApp());

class HelloWorldApp extends StatelessWidget {

  @override

  Widget build(BuildContext context) {

    return MaterialApp(

      title: 'Hello World App',

      home: Scaffold(

        appBar: AppBar(

          title: Text('App Bar Title here'),

        ),

        body: Center(

          child: Text('Hello World'),

        ),

      ),

    );

  }

}

 

 

How to Create a Widget
 

class RandomWords extends StatefulWidget {

  @override

  RandomWordsState createState() => RandomWordsState();

}

 
Add Something to the Widget
 
@override

Widget build(BuildContext context) {

  return Scaffold(

    appBar: AppBar(

      title: Text('Startup Name Generator'),

    ),

    body: _buildSuggestions(),

  );

}

 

Change the Appearance of the Widget
 

class RandomWordsState extends State<RandomWords> {

  final _suggestions = <WordPair>[];

  final _biggerFont = const TextStyle(fontSize: 18.0);

}

 

How to Create Rows and Columns
 

This positions the widget at the start of both the horizontal and vertical columns. Then the widget is still in these columns but the “icon star” is positioned in the “center” or “end” of the row and column.
The cluster of three stars is at the far left of the horizontal row and the top of the vertical column:

Row(
  mainAxisAlignment: MainAxisAlignment.start,

  children: <Widget>[

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

  ],

),

 
The cluster of stars is positioned in the center of the row and column:

  Row(
  mainAxisAlignment: MainAxisAlignment.center,

  children: <Widget>[

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

  ],

),

 

The cluster of stars are now at the end of the horizontal row (far right) and the vertical column (bottom):

 

Row /*or Column*/(

  mainAxisAlignment: MainAxisAlignment.end,

  children: <Widget>[

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

  ],

),

 

This places a space between each star:

 

Row /*or Column*/(

  mainAxisAlignment: MainAxisAlignment.spaceBetween,

  children: <Widget>[

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

  ],

),

 

And this part evens out the spaces between the stars:

 

Row /*or Column*/(

  mainAxisAlignment: MainAxisAlignment.spaceEvenly,

  children: <Widget>[

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

  ],

),

 

This places a space around the stars:

 

Row /*or Column*/(

  mainAxisAlignment: MainAxisAlignment.spaceAround,

  children: <Widget>[

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

  ],

),

 

 

CrossAxisAlignment

The baseline of the text can be aligned using CrossAxisAlignement.Baseline:

Row(

  crossAxisAlignment: CrossAxisAlignment.baseline,

  textBaseline: TextBaseline.alphabetic,

  children: <Widget>[

    Text(

      'Baseline',

      style: Theme.of(context).textTheme.display3,

    ),

    Text(

      'Baseline',

      style: Theme.of(context).textTheme.body1,

    ),

  ],

),

 

This places the large star with the 200 size in the center, aligned in the cross axis:

 

Row /*or Column*/(

  crossAxisAlignment: CrossAxisAlignment.start,

  children: <Widget>[

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 200),

    Icon(Icons.star, size: 50),

  ],

),

 

This positions every star in the center:

 

Row /*or Column*/(

  crossAxisAlignment: CrossAxisAlignment.center,

  children: <Widget>[

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 200),

    Icon(Icons.star, size: 50),

  ],

),

 

 

And this places the stars at the end:

 

Row /*or Column*/(

  crossAxisAlignment: CrossAxisAlignment.end,

  children: <Widget>[

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 200),

    Icon(Icons.star, size: 50),

  ],

),

 

This stretches the entire rows and columns, much like expanding a screen, such as expanding the Microsoft Word screen:

 

Row /*or Column*/(

  crossAxisAlignment: CrossAxisAlignment.stretch,

  children: <Widget>[

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 200),

    Icon(Icons.star, size: 50),

  ],

),

 

 

MainAxisSize

 

This creates the max size of the row and column:

 

Row /*or Column*/(

  mainAxisSize: MainAxisSize.max,

  children: <Widget>[

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

  ],

),

 

Similarly, this creates the minimum size of the row and column:

 

Row /*or Column*/(

  mainAxisSize: MainAxisSize.min,

  children: <Widget>[

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

  ],

),

 

IntrinsicWidth and IntrinsicHeight
 

To create the widest columns and rows, while at the same time the tallest (IntrinsicWidth and IntrinsicHeight):

Widget build(BuildContext context) {

  return Scaffold(

    appBar: AppBar(title: Text('IntrinsicWidth')),

    body: Center(

      child: Column(

        children: <Widget>[

          RaisedButton(

            onPressed: () {},

            child: Text('Short'),

          ),

          RaisedButton(

            onPressed: () {},

            child: Text('A bit Longer'),

          ),

          RaisedButton(

            onPressed: () {},

            child: Text('The Longest text button'),

          ),

        ],

      ),

    ),

  );

}

 

 

To create the widest buttons possible:
 

Widget build(BuildContext context) {

  return Scaffold(

    appBar: AppBar(title: Text('IntrinsicWidth')),

    body: Center(

      child: IntrinsicWidth(

        child: Column(

          crossAxisAlignment: CrossAxisAlignment.stretch,

          children: <Widget>[

            RaisedButton(

              onPressed: () {},

              child: Text('Short'),

            ),

            RaisedButton(

              onPressed: () {},

              child: Text('A bit Longer'),

            ),

            RaisedButton(

              onPressed: () {},

              child: Text('The Longest text button'),

            ),

          ],

        ),

      ),

    ),

  );

}

A stack is great for positioning widgets on top of one another. Here is how to create a stack:

@override

Widget build(BuildContext context) {

  Widget main = Scaffold(

    appBar: AppBar(title: Text('Stack')),

  );

 

  return Stack(

    fit: StackFit.expand,

    children: <Widget>[

      main,

      Banner(

        message: "Top Start",

        location: BannerLocation.topStart,

      ),

      Banner(

        message: "Top End",

        location: BannerLocation.topEnd,

      ),

      Banner(

        message: "Bottom Start",

        location: BannerLocation.bottomStart,

      ),

      Banner(

        message: "Bottom End",

        location: BannerLocation.bottomEnd,

      ),

    ],

  );

}

 

Now you need to place them in a Positioned widget:

 

 

Widget build(BuildContext context) {

  return Scaffold(

    appBar: AppBar(title: Text('Stack')),

    body: Stack(

      fit: StackFit.expand,

      children: <Widget>[

        Material(color: Colors.yellowAccent),

        Positioned(

          top: 0,

          left: 0,

          child: Icon(Icons.star, size: 50),

        ),

        Positioned(

          top: 340,

          left: 250,

          child: Icon(Icons.call, size: 50),

        ),

      ],

    ),

  );

}

 

 

You can use LayoutBuilder instead of guessing the top/bottom values:

 

Widget build(BuildContext context) {

  const iconSize = 50;

  return Scaffold(

    appBar: AppBar(title: Text('Stack with LayoutBuilder')),

    body: LayoutBuilder(

      builder: (context, constraints) =>

        Stack(

          fit: StackFit.expand,

          children: <Widget>[

            Material(color: Colors.yellowAccent),

            Positioned(

              top: 0,

              child: Icon(Icons.star, size: iconSize),

            ),

            Positioned(

              top: constraints.maxHeight - iconSize,

              left: constraints.maxWidth - iconSize,

              child: Icon(Icons.call, size: iconSize),

            ),

          ],

        ),

    ),

  );

}

 

 

Expanded
Expanded creates space between many items:

 

 

Row(

  children: <Widget>[

    Expanded(

      child: Container(

        decoration: const BoxDecoration(color: Colors.red),

      ),

      flex: 3,

    ),

    Expanded(

      child: Container(

        decoration: const BoxDecoration(color: Colors.green),

      ),

      flex: 2,

    ),

    Expanded(

      child: Container(

        decoration: const BoxDecoration(color: Colors.blue),

      ),

      flex: 1,

    ),

  ],

),

 

 

ConstrainedBox
Here is how to have Hello World displayed as a small widget. Most widgets constrain the text, so the letters are close together, and only this small widget will be available to use:

 

Card(child: const Text('Hello World!'), color: Colors.yellow)

 

ConstrainedBox allows you to use the rest of the widget for whatever need:

 

ConstrainedBox(

  constraints: BoxConstraints.expand(),

  child: const Card(

    child: const Text('Hello World!'),

    color: Colors.yellow,

  ),

),

 

 

BoxConstraints creates a widget to whatever size using a min/max and height/width. BoxConstraints.Expand uses the max amount of space.

 

ConstrainedBox(

  constraints: BoxConstraints.expand(height: 300),

  child: const Card(

    child: const Text('Hello World!'),

    color: Colors.yellow,

  ),

),

 

This is the same as the following code:

 

ConstrainedBox(

  constraints: BoxConstraints(

    minWidth: double.infinity,

    maxWidth: double.infinity,

    minHeight: 300,

    maxHeight: 300,

  ),

  child: const Card(

    child: const Text('Hello World!'),

    color: Colors.yellow,

  ),

),

 

Align
CrossAxisAlignment.stretch changes how something stretches, such as a small button or one that fills the entire screen horizontally.

 

Widget build(BuildContext context) {

  return Scaffold(

    appBar: AppBar(title: Text('Align: without Align')),

    body: Column(

      crossAxisAlignment: CrossAxisAlignment.stretch,

      children: <Widget>[

        Align(

          child: RaisedButton(

            onPressed: () {},

            child: const Text('Button'),

          ),

        ),

      ],

    ),

  );

}

 

 

Container
How to use a container. If you don’t specify its size, it will match the child-size:

 

Widget build(BuildContext context) {

  return Scaffold(

    appBar: AppBar(title: Text('Container as a layout')),

    body: Container(

      color: Colors.yellowAccent,

      child: Text("Hi"),

    ),

  );

}

 

To stretch the container, use the double.infinity to change the height and width.

 

Widget build(BuildContext context) {

  return Scaffold(

    appBar: AppBar(title: Text('Container as a layout')),

    body: Container(

      height: double.infinity,

      width: double.infinity,

      color: Colors.yellowAccent,

      child: Text("Hi"),

    ),

  );

}

 

You can change the color using decoration and foregroundDecoration. To create a container as decoration, with a yellow background:

 

Widget build(BuildContext context) {

  return Scaffold(

    appBar: AppBar(title: Text('Container.decoration')),

    body: Container(

      height: double.infinity,

      width: double.infinity,

      decoration: BoxDecoration(color: Colors.yellowAccent),

      child: Text("Hi"),

    ),

  );

}

 

To change the yellow background to orange:
 

Widget build(BuildContext context) {

  return Scaffold(

    appBar: AppBar(title: Text('Container.foregroundDecoration')),

    body: Container(

      height: double.infinity,

      width: double.infinity,

      decoration: BoxDecoration(color: Colors.yellowAccent),

      foregroundDecoration: BoxDecoration(

        color: Colors.red.withOpacity(0.5),

      ),

      child: Text("Hi"),

    ),

  );

}

 

 

Use Transform to change the layout of the widget. This will change the widget to a sideways triangle:
 

Widget build(BuildContext context) {

  return Scaffold(

    appBar: AppBar(title: Text('Container.transform')),

    body: Container(

      height: 300,

      width: 300,

      transform: Matrix4.rotationZ(pi / 4),

      decoration: BoxDecoration(color: Colors.yellowAccent),

      child: Text(

        "Hi",

        textAlign: TextAlign.center,

      ),

    ),

  );

}

 

BoxDecoration
 

To put an image in the background, use DecorationImage:

 

Scaffold(

  appBar: AppBar(title: Text('image: DecorationImage')),

  body: Center(

    child: Container(

      height: 200,

      width: 200,

      decoration: BoxDecoration(

        color: Colors.yellow,

        image: DecorationImage(

          fit: BoxFit.fitWidth,

          image: NetworkImage(

            'https://flutter.io/images/catalog-widget-placeholder.png',

          ),

        ),

      ),

    ),

  ),

);

 

To put a border on the Container:
 

Scaffold(

  appBar: AppBar(title: Text('border: Border')),

  body: Center(

    child: Container(

      height: 200,

      width: 200,

      decoration: BoxDecoration(

        color: Colors.yellow,

        border: Border.all(color: Colors.black, width: 3),

      ),

    ),

  ),

);

 

 

To put a different type of border on the Container. This puts rounded corner on the Container:

 

Scaffold(

  appBar: AppBar(title: Text('borderRadius: BorderRadius')),

  body: Center(

    child: Container(

      height: 200,

      width: 200,

      decoration: BoxDecoration(

        color: Colors.yellow,

        border: Border.all(color: Colors.black, width: 3),

        borderRadius: BorderRadius.all(Radius.circular(18)),

      ),

    ),

  ),

);

 

 

You can use box decoration to change the shape to a circle/ellipse or box/rectangular. If you want to use another shape, you have to use the ShapeDecoration in place of BoxDecoration. Here is how to change the shape to a circle:

 

Scaffold(

  appBar: AppBar(title: Text('shape: BoxShape')),

  body: Center(

    child: Container(

      height: 200,

      width: 200,

      decoration: BoxDecoration(

        color: Colors.yellow,

        shape: BoxShape.circle,

      ),

    ),

  ),

);

 

 

And here is how to give a shadow to the shape:
 

Scaffold(

  appBar: AppBar(title: Text('boxShadow: List<BoxShadow>')),

  body: Center(

    child: Container(

      height: 200,

      width: 200,

      decoration: BoxDecoration(

        color: Colors.yellow,

        boxShadow: const [

          BoxShadow(blurRadius: 10),

        ],

      ),

    ),

  ),

);

 

 

 

In Flutter, you can use three kinds of gradients: RadialGratient, LinearGradient and SweepGradient. Here is how to use the Linear Gradient using the colors of red and blue:

 

Scaffold(

  appBar: AppBar(title: Text('gradient: LinearGradient')),

  body: Center(

    child: Container(

      height: 200,

      width: 200,

      decoration: BoxDecoration(

        gradient: LinearGradient(

          colors: const [

            Colors.red,

            Colors.blue,

          ],

        ),

      ),

    ),

  ),

);

 

 

And here is how to use a blue and yellow radial gradient:
 

Scaffold(

  appBar: AppBar(title: Text('gradient: RadialGradient')),

  body: Center(

    child: Container(

      height: 200,

      width: 200,

      decoration: BoxDecoration(

        gradient: RadialGradient(

          colors: const [Colors.yellow, Colors.blue],

          stops: const [0.4, 1.0],

        ),

      ),

    ),

  ),

);

 

Here is how to use the final gradient, Sweep Gradient:
 

Scaffold(

  appBar: AppBar(title: Text('gradient: SweepGradient')),

  body: Center(

    child: Container(

      height: 200,

      width: 200,

      decoration: BoxDecoration(

        gradient: SweepGradient(

          colors: const [

            Colors.blue,

            Colors.green,

            Colors.yellow,

            Colors.red,

            Colors.blue,

          ],

          stops: const [0.0, 0.25, 0.5, 0.75, 1.0],

        ),

      ),

    ),

  ),

);

 

 

Here is how to use backgroundBlendMode. It’s the most complicated feature of BoxDecoration. You can combine colors and gradients and anything else you want using BlendMode. The following code is an image while at the same time using a gradient on the image.

 

Scaffold(

  appBar: AppBar(title: Text('backgroundBlendMode')),

  body: Center(

    child: Container(

      height: 200,

      width: 200,

      foregroundDecoration: BoxDecoration(

        backgroundBlendMode: BlendMode.exclusion,

        gradient: LinearGradient(

          colors: const [

            Colors.red,

            Colors.blue,

          ],

        ),

      ),

      child: Image.network(

        'https://flutter.io/images/catalog-widget-placeholder.png',

      ),

    ),

  ),

);

 

 

Here is another way of writing the code:
Scaffold(

  appBar: AppBar(title: Text('backgroundBlendMode')),

  body: Center(

    child: Container(

      decoration: BoxDecoration(

        image: DecorationImage(

          image: NetworkImage(

            'https://flutter.io/images/catalog-widget-placeholder.png',

          ),

        ),

      ),

      child: Container(

        height: 200,

        width: 200,

        foregroundDecoration: BoxDecoration(

          backgroundBlendMode: BlendMode.exclusion,

          gradient: LinearGradient(

            colors: const [

              Colors.red,

              Colors.blue,

            ],

          ),

        ),

      ),

    ),

  ),

);

React JS Cheat Sheet
VUE.JS Cheat Sheet to Use in 2021
JavaScript Cheat Sheet for Web Development?
Materials
Here is how to make a rectangle with cut corners:

Scaffold(

  appBar: AppBar(title: Text('shape: BeveledRectangleBorder')),

  body: Center(

    child: Material(

      shape: const BeveledRectangleBorder(

        borderRadius: BorderRadius.all(Radius.circular(20)),

        side: BorderSide(color: Colors.black, width: 4),

      ),

      color: Colors.yellow,

      child: Container(

        height: 200,

        width: 200,

      ),

    ),

  ),

);

 

 

Slivers
 

SliverFillRemaining is useful for centering text. In this case, it’s centering an image, as follows:

 

Scaffold(

  appBar: AppBar(title: Text('SliverFillRemaining')),

  body: CustomScrollView(

    slivers: [

      SliverFillRemaining(

        hasScrollBody: false,

        child: Column(

          mainAxisAlignment: MainAxisAlignment.center,

          children: const [

            FlutterLogo(size: 200),

            Text(

              'This is some longest text that should be centered'

              'together with the logo',

              textAlign: TextAlign.center,

            ),

          ],

        ),

      ),

    ],

  ),

);

 

SliverFillRemaining can also make use of the remaining space and widen whatever is being used, such as an image like in the above example. A widget called CustomScrollView is used last to fill in the remaining space.

 

Scaffold(

  appBar: AppBar(title: Text('SliverFillRemaining')),

  body: CustomScrollView(

    slivers: [

      SliverList(

        delegate: SliverChildListDelegate(const [

          ListTile(title: Text('First item')),

          ListTile(title: Text('Second item')),

          ListTile(title: Text('Third item')),

          ListTile(title: Text('Fourth item')),

        ]),

      ),

      SliverFillRemaining(

        hasScrollBody: false,

        child: Container(

          color: Colors.yellowAccent,

          child: Column(

            mainAxisAlignment: MainAxisAlignment.center,

            children: const [

              FlutterLogo(size: 200),

              Text(

                'This is some longest text that should be centered'

                'together with the logo',

                textAlign: TextAlign.center,

              ),

            ],

          ),

        ),

      ),

    ],

  ),

);

Sized Box
Sized Box is similar to ConstrianedBox. Here is a basic example using the “Hello World!” again.

SizedBox.expand(

  child: Card(

    child: Text('Hello World!'),

    color: Colors.yellowAccent,

  ),

),

 

SizedBox can add space or margins between objects. In this example, it’s space between stars:

Column(

  children: <Widget>[

    Icon(Icons.star, size: 50),

    const SizedBox(height: 100),

    Icon(Icons.star, size: 50),

    Icon(Icons.star, size: 50),

  ],

),

 

You can also hide and show widgets, like as follows:

Widget build(BuildContext context) {

  bool isVisible = ...

  return Scaffold(

    appBar: AppBar(

      title: Text('isVisible = $isVisible'),

    ),

    body: isVisible

      ? Icon(Icons.star, size: 150)

      : const SizedBox(),

  );

}

 

SafeArea
SafeArea is used so that your work won’t overlap the time in the upper right-hand corner or anything else. It will fit into a safe working area, like so:

Widget build(BuildContext context) {

  return Material(

    color: Colors.blue,

    child: SafeArea(

      child: SizedBox.expand(

        child: Card(color: Colors.yellowAccent),

      ),

    ),

  );

}

 

Other Flutter Basics
Here are other ways of doing the same function listed above. Much like other software, there are various ways of performing the same action. You will notice small differences in the code. Here is another way to write the Hello World in Flutter.

 

import 'package:flutter/material.dart';

main() => runApp(HelloApp());

class HelloApp extends StatelessWidget {

  Widget build(BuildContext context) {

    return MaterialApp(

      home: Material(

        child: Text("Hello world!"),

      ),

    );

  }

}

 

Here is a Scaffold example:
 

Scaffold(

  appBar: AppBar(

    title: Text("I'm aan AppBar."),

  ),

  body: Center(

    child: Text("I'm a Text widget."),

  ),

  floatingActionButton: FloatingActionButton(

    child: Icon(Icons.ac_unit),

  ),

  drawer: Drawer(

    child: Center(child: Text("I'm a drawer.")),

  ),

)

 

  <b>How to run the Cupertino App:</b>

import 'package:flutter/cupertino.dart';

void main() => runApp(CupterinoApp());

class CupterinoApp extends StatelessWidget {

  @override

  Widget build(BuildContext context) {

    return CupertinoApp(

      home: CupertinoPageScaffold(

        navigationBar: CupertinoNavigationBar(

          backgroundColor: Color.fromRGBO(66, 165, 245, 1.0),

          middle: Text("I'm a navigation bar"),

        ),

        child: Center(

          child: Text('Hello from Cupertino, Californa!'),

        ),

      ),

    );

  }

}

 

  <b>Create a column in Flutter:</b>
Column(

  mainAxisAlignment: MainAxisAlignment.center,

  children: [

    Text("I'm on top."),

    Text("I'm in the middle."),

    Text("I'm the bottom."),

  ],

)

 

  <b>Response to a button press:</b>
  
import 'package:flutter/material.dart';

void main() => runApp(ButtonDemo());

class ButtonDemo extends StatelessWidget {

  Widget build(BuildContext context) {

    return MaterialApp(

      home: MyHomePage(),

    );

  }

}

 

class MyHomePage extends StatefulWidget {

  _MyHomePageState createState() => _MyHomePageState();

}

 

class _MyHomePageState extends State {

  String _whatToDisplay;

  void initState() {

    _whatToDisplay = 'Click Me';

  }

 

  void _doSomething() {

    setState(() {

      _whatToDisplay = 'Thank you for clicking';

    });

  }

 

  Widget build(BuildContext context) {

    return Scaffold(

      body: Center(

        child: RaisedButton(

          child: Text(_whatToDisplay),

          onPressed: _doSomething,

        ),

      ),

    );

  }

}

 

  <b>Useful layout widgets:</b>

Material(

  child: SafeArea(

    child: Column(

      children: [

        Expanded(

          child: Container(

            height: 50.0,

            color: Colors.blue,

          ),

        ),

        SizedBox(

          height: 50.0,

        ),

        Container(

          alignment: Alignment.bottomRight,

          height: 100.0,

          color: Colors.blue,

          child: Padding(

            padding: const EdgeInsets.all(20.0),

            child: Text(

              'Hello',

              style: TextStyle(backgroundColor: Colors.red),

            ),

          ),

        ),

      ],

    ),

  ),

)

 

  <b>Text field:</b>

class _MyHomePageState extends State {

  final _myController = TextEditingController();

 

  @override

  void dispose() {

    _myController.dispose();

    super.dispose();

  }

 

  @override

  Widget build(BuildContext context) {

    return Material(

      child: Center(

        child: Column(

          mainAxisAlignment: MainAxisAlignment.center,

          children: [

            TextField(

              decoration: InputDecoration(labelText: "Type something:"),

              controller: _myController,

            ),

            RaisedButton(

              child: Text("UPPERCASE"),

              onPressed: () =>

                  _myController.text = _myController.text.toUpperCase(),

            ),

          ],

        ),

      ),

    );

  }

}

 

  <b>Slider in Flutter:</b>
class _MyHomePageState extends State {

  double _sliderValue = 1.0;

  void _refreshSlider(double newValue) {

    setState(() {

      _sliderValue = newValue;

    });

  }

  @override

  Widget build(BuildContext context) {

    return Material(

      child: Center(

        child: Column(

          mainAxisAlignment: MainAxisAlignment.center,

          children: [

            Text(_sliderValue.toStringAsFixed(2)),

            Slider(

              value: _sliderValue,

              onChanged: _refreshSlider,

              min: 1.0,

              max: 10.0,

            )

          ],

        ),

      ),

    );

  }

}

 

  <b>Create radio buttons:</b>
class _MyHomePageState extends State {

  int _radioValue;

 

  void _refreshRadio(int newValue) {

    setState(() {

      _radioValue = newValue;

    });

  }

  @override

  Widget build(BuildContext context) {

    return Material(

      child: Center(

        child: Column(

          mainAxisAlignment: MainAxisAlignment.center,

          children: [

            Text(_radioValue?.toString() ?? 'Select One'),

            Row(

              mainAxisAlignment: MainAxisAlignment.center,

              children: [

                Text('0'),

                Radio(

                    value: 0,

                    groupValue: _radioValue,

                    onChanged: _refreshRadio),

                Text('1'),

                Radio(

                    value: 1,

                    groupValue: _radioValue,

                    onChanged: _refreshRadio),

                Text('2'),

                Radio(

                  value: 2,

                  groupValue: _radioValue,

                  onChanged: _refreshRadio,

                )

              ],

            ),

          ],

        ),

      ),

    );

  }

}

 

  <b>Basic navigation:</b>
class FirstPage extends StatelessWidget {

  @override

  Widget build(BuildContext context) {

    return Material(

      child: Center(

        child: RaisedButton(

          child: Text('Go to second page'),

          onPressed: () {

            Navigator.push(

              context,

              MaterialPageRoute(

                builder: (context) => SecondPage(),

              ),

            );

          },

        ),

      ),

    );

  }

}

 

class SecondPage extends StatelessWidget {

  @override

  Widget build(BuildContext context) {

    return Material(

      child: Center(

        child: RaisedButton(

          onPressed: () {

            Navigator.pop(context);

          },

          child: Text('Go back!'),

        ),

      ),

    );

  }

}

 

 

  <b>How to create a list</b>
List movieName = [

  "Casablanca",

  "Citizen Kane",

  "Lawrence of Arabia",

];

 

ListView.builder(

  itemCount: movieName.length,

  itemBuilder: (context, index) {

    return ListTile(

        title: Text(movieName[index]),

        onTap: () => _goToDetailPage(movieName[index]));

  },

)

 

  <b>How to create an animation</b>
class MyHomePageState extends State

    with SingleTickerProviderStateMixin {

  Animation animation;

  AnimationController controller;

 

  @override

  void initState() {

    super.initState();

    controller =

        AnimationController(duration: const Duration(seconds: 3), vsync: this);

    animation = Tween(begin: 100.0, end: 500.0).animate(controller)

      ..addListener(() {

        setState(() {});

      });

    controller.forward();

  }

 

  @override

  Widget build(BuildContext context) {

    return Material(

      child: Stack(

        children: [

          Positioned(

            left: 150.0,

            top: animation.value,

            child: Icon(

              Icons.music_note,

              size: 70.0,

            ),

          ),

        ],

      ),

    );

  }

 

  @override

  void dispose() {

    controller.dispose();

    super.dispose();

  }

}
