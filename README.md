If you're not lucky (or patient enough!) here is an example diff where the
output changed. Notice the `dup`

```diff
--- output-1.js	2017-03-31 22:26:02.000000000 +0100
+++ output-35.js	2017-03-31 22:26:12.000000000 +0100
@@ -4,14 +4,13 @@
 module.exports="a string";
 },{}],3:[function(require,module,exports){
 var c=require("./c");module.exports=[c];
-
 },{"./c":2}],4:[function(require,module,exports){
 require("./d");
 
 },{"./d":3}],5:[function(require,module,exports){
 arguments[4][2][0].apply(exports,arguments)
 },{"dup":2}],6:[function(require,module,exports){
-var c=require("./c");module.exports=[c];
-},{"./c":5}],7:[function(require,module,exports){
+arguments[4][3][0].apply(exports,arguments)
+},{"./c":5,"dup":3}],7:[function(require,module,exports){
 require("../a"),require("./d");
 },{"../a":4,"./d":6}]},{},[1]);
```
