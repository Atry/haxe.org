##### 2008-04-05: __1.19__

* fixed flash9 Array.toString
* fixed inline return bug
* added haxe.rtti.Generic behavior
* added haxe.FastList
* bugfix to prevent recursive anonymous
* fixed some incorrectly reported "recursive inline" errors
* fixes in genas3 + genswf9 for Dynamic/* in methods
* {} is now an empty object and not an empty block
* fixed some verify errors left in flash9
* fixed private/protected differences in gen-hx-classes
* genswf9 : allowed to store a Class in a typed register
* fixed switch-on-bool (don't use matching)
* genswf9 : optimized switch on ints
* some renames in haxe.rtti.Type
* added flash.utils.TypedDictionary for F9
* genswf9 : fixe debug filename with inline code
* fixed completion for packages starting with 'a' or 'z'
* added flash9.Lib.as
* prevent double Movieclip class declaration when linking flash9 lib
* allow numerical operations on type parameters constraint by Float
* genswf9 : fixed dynamic inheritance

##### 2008-02-23: __1.18__

* some optimization and bugfix for as3 codegen
* bugfix : allow bitmaps and fonts classes for F9 library
* bugfix : neko.Web.setCookie
* bugfix : as3 switches in -swf-lib, and enable to "repair" corrupted as3 bytecode
* fixed --i return value in flash9
* fixed some transforms in flash9
* added js.Selection
* simplified js.Dom (more events)
* added haxe.xml.Fast.innerHTML
* added Reflect.compare
* fixed "".split() in Neko (now returns [""] instead of [])
* bugfix for swf-lib f9 classes ordering
* added EReg.customReplace
* added neko.Lib.lazyLoad and improved neko.net.Poll for Neko 1.6.1
* prevented static fields in interfaces
* added neko.Sys.cpuTime()
* fix for protected as3 classes
* added support for flash9 XML (in flash.xml package)
* added neko.vm.Tls for Neko 1.6.1
* added --no-inline
* renamed neko.zip.File to neko.zip.Reader
* added neko.zip.Writer and neko.zip.CRC32
* fixed multilevel Transform.block_vars
* added js.SWFObject
* fixes for if/switch with null or Null<T> on Flash9

##### 2008-01-13: __1.17__

* fixed Int32.compare, added Int32.read and Int32.write
* fixed type of unitialized registers in flash9
* fixed Sqlite transactions (commit and rollback now restart a transaction)
* several flash9 optimizations
* flash9 debug support (with -D fdb)
* set align to TopLeft if not defined for flash9
* added neko.vm.Gc
* fixed Null should not be a value
* bugfix in serialization format with USE_ENUM_INDEXES
* added apis in DateTools for time manipulation
* bugfix in flash9 : strictly typed local vars used in local functions
* always force swf version and sandbox redefinition
* added as3hl layer
* merge as3 classes
* use flash9 fast switch for enums
* always use match for enums (no switch even if constant)
* fixed DateTools.format %I and %l in Flash/JS
* securized Hash for JS and Flash
* compiletime F9 class generation for F8 swflib
* optimized for loops (Array and IntIter)
* added #line support
* more f9 Null<T> support for "if" and array declarations
* more neko.Web.setCookie parameters
* added "inline" for methods and static vars
* fixed % type in flash9

##### 2007-10-31: __1.16__

* use _sans font for default flash traces (better Linux support)
* fixed haxe.remoting.Connection compilation for Flash<8
* added fix to prevent 64K identifiers limit on Flash<9
* ensure order of anonymous fields initialization
* fixed haxe.remoting.Connection.urlConnect in JS
* use amortized O(1) for Neko Array implementation
* ndlls libraries should now use .neko() instead of __a
* allowed 'u' utf8 for regexp (needs Neko 1.6.1 regexp.ndll on windows)
* onclick and onsubmit JS events returns Bool
* fixed inherited constructor of extern class was always private
* fixed Ereg.split without 'g' flag on JS/Flash9
* fixed haxe.Stack in JS without -debug
* added support for -D no-swf-compress
* fixed ByteArray.readObject
* fixed implements Dynamic in Flash9
* removed neko.io.FileInput.eof, fixed neko.io.Input.readLine
* fixed haxe.Template for Flash9
* added neko.Sys.command optional array of arguments
* removed haxe.Proxy
* added flash.XMLRequest
* fixed Type.enumParameters for Neko
* guaranteed order of Type.getEnumConstructs same as code
* used index-based dispatch for enums
* added Type.enumIndex
* fixed enum.toString for Flash and JS
* support for -Dnetwork-sandbox
* trim -cp and -resource
* various genas3 fixes

##### 2007-08-29: __1.15__

* fixed bug with Enum.construct when Enum have type parameters
* change with "untyped" : arguments types are checked (because of opt select)
* haxedoc : fixed type parameters display
* fix for JS and Flash9 XML parser : allow newlines in attributes
* disable Flash9 resources with AS3Gen
* error on extra anonymous fields
* error on too much big neko array declaration (neko 1.6 max_stack limit)
* fixed Flash9 statics slots (FP 9,0,60 compatibility)
* fixed Flash9 Type.getClassName
* optional enums arguments on Flash9 are now automatically Null
* forbid usage of type parameters in static functions
* fixed Std.int with negative numbers
* fixed some F9 issues with haXe-specific Array, Date and Math methods
* used AS3 namespace for F9 Array and String instance methods
* fixed F9 with uninitialized integer registers
* fixed F9 + operator with Dynamic/Null operands
* added Enum subtyping
* fix with remoting threadserver and exceptions
* fixed Flash9 dynamic runtime type field access
* fixed very tricky typing bug with constructors inheritance
* fixed some documentation related parser bug
* fixed stack overflow with static setter
* fixed package completion bug when -cp points to an not existing dir
* fix duplicate sandboxes tags with -swf
* __resolve in haXe Remoting is now public

##### 2007-07-25: __1.14__

* fixed no error when invalid "catch" expression
* remove variance
* fixed prototype bug in neko when "Main" class is defined
* fixed flash9 xml iterator methods
* bugfix in flash9 ByteArray serialization
* fixed genAS3 conflicting classes and interfaces
* preserve neko output file extension
* added flash.Event for Flash9
* added --no-output
* fixed neko.net.Socket peer and host methods
* added neko.io.Process and neko.vm.Ui
* added haxe.xml.Proxy
* some flash6 fixes
* allowed simplequotes for xml attributes in Flash9 and JS
* flash9 optimizing compiler
* new faster neko binary AST
* added haxe.remoting.NekoSocketConnection and SocketProtocol
* don't allow for...in iteration with Dynamic or Unknown
* added flash9 resources
* fixed precedence of ternary operator ?:

##### 2007-05-18: __1.13__

* fixed bug with local variable masking package in catch type
* fixed "Not_found" when enum params differs
* added "override" for AS3 generator
* fixed stack overflow in typedefs
* added haxe.Timer.queue, removed delayedArg (use callback instead)
* fixed haxe.remoting.SocketConnection (msg invertions might occur)
* add uniqueness check for switch constants
* js : HtmlCollection and MetaDom.childNodes are not true Arrays
* allowed semicolon after typedef declaration
* fixed in-loop closure usage of "for" variable for Flash and JS
* added neko.net.ThreadRemotingServer.onXml (to handle crossdomain xml)
* more accurate stack trace for socket remoting
* prevent some memory leak in haxe.Timer / JS
* added flash fullscreen support
* added cond?a:b syntax support
* added utf8 buffer api
* added haxelib "dev" mode
* renamed Http.asyncRequest to customRequest
* add classes to Neko module export table
* fixed parametrized enums for Flash6
* fixed bug with completion and interfaces
* fixed --flash-use-stage in Flash9

##### 2007-03-06: __1.12__

* added flash lite support with -D flash_lite
* bugfix for Unknown<X> should Unknown<X>
* prevent some exceptions in neko.net.ProxyDetect
* fixed ByteArray serialization
* added neko.Int32
* added -x for fast neko scripting
* prevent locals from breaking class access (works with imports)
* fix in function overriding subtyping
* added haxe.remoting.FlashJsConnection
* fixed tar support in neko.zip.File
* ide completion support using --display
* give access to neko.net.Host ip (as Int32)
* fixed bug when calling super.UpperCaseMethod()
* hide additional flash Array methods
* allow leading comma in anonymous types
* added haxe.Public interface
* added AS3 code generator
* field lookup gives priority to superclass over interfaces
* improved haxedoc output
* fixed bug in neko regexp split/replace when empty match at eol
* fixed bug in flash 6-7-8 resources generation

##### 2007-01-28: __1.11__

* changed StringBuf.add implementation
* added haxe.Firebug
* allowed variable return type for overriden/implemented methods
* display error position in front of each error line
* improved error messages when optional arguments not matched
* added neko.io.Path
* added neko.net.ProxyDetect
* bugfix in unify : prevent recursive anonymous objects
* haxe.Http call "prepare" only if size is known
* added multiple expressions in "case"
* serialization : deprecated old string format, use urlEncode/Decode
* added flash9 bytearray serialization (to binary string, for neko com)
* fixed Type.typeof on some flash9 instances
* no more dontUseCache (haxe.Serializer.USE_CACHE, default to false)
* small genxml/haxedoc improvements
* added Type.enumEq
* local function parameters are now inferred in several cases
* optional RTTI for Spod Object
* bugfix related to callback in neko code generator
* more type error stack (now includes type parameters)
* type system fixes in anonymous subtyping
* added Iterable<T>, changed Lambda
* added TAR and GZIP support to neko.io.Zip
* compute minimal array content type
* fixes in enum switchs

##### 2007-01-01: __1.10__

* fix in haxe.remoting.SocketConnection.readAnswer
* fix in postfix incr/decr and getter/setter
* added haxe.Http.fileTransfert for Neko
* fixed haxelib to 1.02 (use multipart file transfert)
* fixed Array.reverse
* added flash.Lib.getURL and fscommand for Flash9
* fixed some ignored parse errors
* fixed minor syntax : immediate object access
* allow extend/implements a typedef
* fixed Flash9 AMF remoting
* fixed Flash9 bugs in Date object
* fixed dynamic Array typing bug
* allowed typedef private field access
* added Class<T> base class type
* AsyncConnection.call callback is now optional
* fixed if/switch with no else/default compilation
* moved Reflect.createInstance to Type
* added Reflect.makeVarArgs
* haXelib 1.03 : several developers per project + web interface

##### 2006-11-22: __1.09__

* added neko.vm.Module and neko.vm.Loader
* haxelib : allowed spaces in "run" arguments
* allowed Thread comparison
* fixed bug in SWF6 compilation
* allowed either Mysql or Mysql5 usage
* replaced db.Connection.hasFeature by db.Connection.dbName
* added Socket.custom field
* moved neko.Thread to neko.vm.Thread
* define haxe_109 (for api changes)
* fixes in haxe.remoting.Connection and haxe.Unserializer for F9
* added haxe.remoting.Connection.urlConnect for JS
* allowed private typedef fields
* added neko.net.ThreadServer, ThreadRemotingServer and Poll
* removed neko.net.RemotingBuffer
* relaxed enums switchs (allow value in first case)
* changed "cast" codegeneration (fix some F9 usages)
* change in POST data handling in mod_neko (max 256K, except multipart)
* added neko.Web.getClientHeaders and neko.Web.flush
* "callback" is now a keyword
* fixed stack overflow when typedef = Dynamic
* fixed Reflect.createInstance on F9
* Array : slice optional length, fixed neko slice & splice
* + fixed cast return type

##### 2006-10-29: __1.08__

* fixed bug in flash -debug
* fixed Sqlite result .length
* fixed missing "." in OSX/Linux default classpath
* fixed haxelib NDLL autoloading on OSX
* fixed bug in deserialization of "\\\r" sequence
* added inheritance and fields getter/setter to xml output
* haxedoc 2.0
* fixed neko native enum serialization
* fixed "all constructors matched" for enums without params
* fixed returned value semantics in neko (prevent remoting leak)
* more documentation
* added haxe.rtti package (classes can implement haxe.rtti.Infos)
* fixed windows line endings in exclude files under linux/osx
* fixed small bug in "cast" syntax
* added "callback" for partial function application
* added --auto-xml for future haxeFD usage
* fixed Reflect.isFunction
* minor bugfix in JS code generator
* new neko.net package
* allow recursive remoting proxys (skip instead of error)
* added neko.Thread and neko.Lock MultiThread classes
* added neko.net.ServerLoop for multiple clients handling

##### 2006-09-11: __1.07__

* fixed resources in Neko
* typedef, override, package and f9dynamic are now keywords
* slighly changed error format output
* fixed "undefined" serialization and Type.typeof
* some fixes in haxelib
* set default classpath for non windows systems
* added variance
* fixed bug in bounded type parameters
* fixed scope bug in try/catch with Flash9
* added remoting over XMLSocket and LocalConnection for Flash9
* fixed Std.is(*,null) = false
* allowed >64K haXe/neko strings
* -debug and stack traces support for Flash and JS
* minor changes in xml output

##### 2006-08-28: __1.06__

* allowed extern enums
* use only matching construct when parameters are matched
* fixed bug preventing & char to be sent between JS and Flash remoting
* improved flash9 api (more strict)
* flash9 xml : use JS ReXml parser
* added neko.io package (Input/Output)
* moved neko.File and neko.Socket to neko.io package
* fixed flash optional arguments (when extending flash.MC)
* fixed neko native serialization problems
* variable modification does not have side effects in 'for x in a...b'
* jit disabled by default for neko web server
* enable flash7-8 libraries usage from flash9
* unknown identifier become "class not found" when representing a classpath
* changed haxe.PosInfos handling
* added -debug (removed --flash-debug) effective on flash9 and neko only now
* added Type.typeof
* improved Serializer speed
* added Serialization support for Date, Hash, IntHash, List
* added flash9 and JS IE/Opera class reflection
* added haxe.xml.Check and haxe.xml.Fast
* added Xml.parent
* added haxelib
* added ArrayAccess interface

##### 2006-08-16: __1.05__

* moved Md5 to haxe package.
* some method renamed in neko.FileSystem.
* added neko.remoting.Server.setLogger
* fixed bug in haxe.Serializer on neko (was preventing List serialization)
* fixed bugs in haXe.Unserializer on neko (invalid enum tag & pbs with UTF8 strings)
* fixed sqlite escape & quote , added BOOL support
* allowed direct property access in getter/setter (prevent rec loop)
* allowed event-driven neko http requests
* forbidden "name" static in js
* don't allow variable redeclaration in subclasses
* added && || and ! in conditional compilation rules
* metas : removed __construct__ and class.toString.
* metas : __super__ and __interfaces__ now optional
* added Type api (seperated from Reflect)
* flash 9 support

##### 2006-07-25: __1.04__

* added macros in haxe.Template
* allowed static variables access from a signature shortcut
* allowed new Signature when signature is a class
* fixed : modulo priority is now higher than mult and div
* fixed bug in haxe.Proxy generation
* fixed more stack overflows with recursive signatures
* fixed bug in class <: anonymous subtyping (inherited fields)
* override is not mandatory by default (need --override)
* added neko just-in-time
* fixed bugs in haxe.Serializer and haxe.Unserializer (enum format change)
* changed "signature" by "typedef" (more comprehensible)
* restricted objects comparisons
* fixed bug with js operator priority
* improved performances for haxe.Serializer and haxe.Unserializer
* fixed bug in static variable lookup (should look class in the last case)
* prevented several prints of "not enough arguments".

##### 2006-06-23: __1.03__

* haxedoc executable now part of the distribution
* removed selectDB from the neko.db.Connection API
* added optional parameters with selection
* removed --no-flash-opt-args
* changes in SWF packages handling
* fixed optional leading comma in anonymous object and array values
* fixed bug in inheritend constructor type parameters
* fixed bug in type_field with inherited type parameters
* added haxe.Proxy
* added code transformations for swf/js block variables
* fixed very tricky bug with constraint parameters used together with polymorphic methods
* added selective import (import x.y.Class.InnerType)
* added optional enum constructor parameters
* added opened anonymous types (no more Unknown has no field...)
* fixed "MovieClip extends flash.MovieClip".
* added Reflect.copy
* added neko.Random
* added Date.fromString
* fixed bug in haxe.Unserializer, slighlty optimized haxe.Serializer
* added __setfield magic (complete __resolve)
* added explicit override when overriding methods

##### 2006-06-08: __1.02__

* fixed stack overflow when recursive class <: recursive signature
* improved a bit commandline : allow several hxml arguments
* added {> Class, fields... } types declarations
* added cast without type (less dangerous than untyped)
* no stage objects by default, added --flash-use-stage
* added haxe.remoting.DelayedConnection
* added -exclude
* removed classpath from neko debug infos filenames
* fixed bug in Neko empty Array.pop and Neko EReg.replace ""
* fixed nodeValue for Neko XML comments, doctype, prolog
* improved DocView : formating, signatures, files generation
* added neko.zip package
* fixed bug in neko.File binary flags
* fixed problems when downloading large files using haxe.Http under Neko
* neko.db.Connection and neko.db.ResultSet are now interfaces
* added neko.db.Sqlite and neko sqlite ndll
* mod_neko2.ndll for Apache2 in Windows distribution
* fixed bug in static properties method resolution
* change js.Dom : use cascading signatures and improved api
* added haxe.unit Unit test framework

##### 2006-05-25: __1.01__

* added neko.Utf8
* Serializer/Unserializer now support utf8 strings
* allowed subtyping of prop accesses public/private when implementing an interface
* removed "eval" from Remoting APIs (only calls - more easy to handle).
* added flash6 support
* fixed Std.is on different platforms (interfaces implements interface)
* added AsyncConnection.amfConnect for flash
* added SWF overflow checks
* changed "property" to "var"
* don't allow monorph unification with Dynamic (more safe)
* allowed multiple parsing and typing errors
* review and completed commandline options
* error on backwards constant integer iterators
* remoting proxy constructor is now public
* fixed -swf-header override the swflib background color
* moved all remoting classes into the haxe.remoting package
* added haxe.remoting.LocalConnection

##### 2006-05-17: __1.0__

* fixed small bugs in JS Xml Parser (empty attribute, newlines in attributes)
* added default Content-Type for haxe.Http in JS
* haxe.AsyncConnection : onError should not be call if error occur in onData
* fixed infinite loop if haxe.Unserializer.readDigits reach eof on JS/Flash
* fixed bugs in neko.Web and neko.Sys (some methods returning "null" instead of null)
* added neko.Socket.setBlocking for nonblocking sockets
* fixed bug in js generator when using cascading iterators
* fixed typing bug when overloading parametrized method
* fixed bug in js generator when "try" without curly braces.
* allowed enum catching
* added remoting proxys
* allowed neko.Web API commandline emulation outside mod_neko
* removed subtyping Anon :> Instance
* added signatures, Iterator is now a signature
* getter/setter and public/private unification
* allowed anonymous declaration with interface-style syntax (for signatures)
* optimized code generated for underscore in enum matches parameters
* fixed flash/js String.charCodeAt(outside) => null
* fixed neko charAt(outside) => ""
* added errors for strings containing \0 in JS and Flash
* added HAXE_LIBRARY_PATH environment variable support
* fixed interfaces inheritance : can't extend, can implement (type-sums)
* fixed fixed >64K resource bug in SWF
* fixed newline problems with Flash/JS Connection

##### 2006-05-02: __RC1__

* added the Socket class
* fixed a bug of returned value in neko with 6 or more parameters
* added "Missing type" error for catchs.
* added regular expressions (still missing Flash implementation)
* fixed type printing and parenthesis in type declarations
* different behavior when elements removed during Array.iteration
* fixed genswf : local variables used in for...function
* improved type parameters structure coherency
* enable usage of Spod without Transaction
* implemented neko.db.Transaction.isDeadlock
* slighly relaxed one of the javascript generator constraint
* added haxe.Template
* moved Log , PosInfos and ImportAll to haxe package
* completed private class/interface/enum support
* removed Array.indexes
* added __resolve compile-time support when class implement Dynamic
* added haxe Remoting
* added "module with different case" error (for windows)
* added Reflect.resolveClass, Reflect.resolveEnum, Reflect.setPrototype
* added access to classes by name in genneko
* added enum.__ename__
* fixed Std.is(e,enum)
* fixed infinite loop in neko EReg split/replace and epsilon matching
* added neko native serialization support
* fixed syntax for multiple constraints in type parameter
* added recursive type parameters contraints (T : C<T> constraints)
* updated Xml handling

##### 2006-04-17: __beta 5__

* fixed bug : continue in do...while
* changed typing order for do...while (infer condition after block)
* fixed JS "catch" generation
* fixed extending flash.* extern class
* fixed bug in neko generator w/ closures
* fixed bug in js generator (return switch need correct "this" context)
* fixed bug in for x in a...b : invalid local variables overridding
* added properties
* fixed bug in js generator : while...switch...break
* new List implementation
* can use static function __init__ on every platform
* bug fixes in Reflect.fields
* added Hash.remove, changed Hash/JS implementation
* added flash __delete__ support
* added neko.db.Object, Manager, Transaction
* fixed neko class.__interfaces__
* added "assigning a value to itself" error
* added automatic PosInfos when is last parameter
* added polymorphic methods
* added check_flash_args support

##### 2006-04-02: __beta 4__

* fixed javascript events case
* fixed invalid use of physeq
* fixed + type inference
* added -altfmt
* allowed anonymous <: class subtyping
* relaxed unifications of expressions in "for" and "while"
* more methods in List
* syntax changes : mandatory parenthesis for "for" and "while"
* allowed any kind of identifier almost everywhere
* moved tools, flash, js and neko inside "std"
* no need for 0x in flash header bgcolor
* added -res
* fixed type parameter contraint holes
* Std.is Dynamic always returns true
* added Enum.toString
* neko : env locals can be modified in inner functions
* completed js keywords list in generator
* added Reflect.typeof
* prioritize neko.Lib.load static calls
* fixed bugs in for...in optimization with continue
* fixed Reflect fields, added documentation, added Class
* added javascript closures, fixed null closures on flash and Neko
* added javascript __init__ statics and js.XMLHttpRequest
* added neko.Stack
* fixed bug in Std.ord
* convert neko string to haxe string on catch
* automaticaly creates empty clips for classes extending flash.MovieClip
* unify stack : several meaningful unification errors
* added cast operation and keyword

##### 2006-03-11: __beta 3__

* javascript generator
* optimized for in interval
* renaming of locals (name must be unique)
* added uncaught exceptions handling in Flash
* fixed Bool.true == true and Bool.false == false on all platforms
* fixed matching on Bool different from enums
* removed -fplayer (use -D instead) and added -fheader
* fixed infinity is Int
* added "here" special identifier
* neko Apis : File, FileSystem, Sys
* added base JS API

##### 2006-02-19: __beta 2__

* renamed neko.db.Result to neko.db.ResultSet
* added Date support for Mysql results
* added private fields for static class anonymous types
* disambigous >=, >>= and >>>=
* fixed inheritance bug in swf and neko generators
* improved function parameters type error reporting.
* allowed variable number of args for flash.* constructors.
* added Math.random(), Reflect.empty()
* added flash.XMLSocket and flash.Timer classes
* completed Std class with conversion functions and others.
* completed flash.Lib class with flash toplevel functions.
* fixed bugs in neko webserver

##### 2006-02-04: __beta 1__

* allowed array literals to be dynamic
* use neko 1.2 commandline and prototypes
* changed #cond to #if cond for conditional compilation
* all fields are defined to null by default
* defined __class__ and other meta accesses for Flash and Neko
* fixed type hole for compiler-know types (should not resolve using imports)
* changed packages : neko.* and flash.* (with protection)
* added Lazy types : type the fields when they are needed with recursion
* untyped accesses are monomorphs, not dynamics
* generated __string check that toString() return an object
* XmlParser and other APIs for Neko
* fixed escaped chars in Neko generation
* conservative static initialization order
* allowed no type parameters for new Class
* function types carry parameter names
* anonymous types contain private variables (for private static accesses)
* added optional name for anonymous types in typer (for static accesses)
* private classes and enums (partial support)
* improved error message for invalid number of arguments
* flash extern classes can take variable number of args.
* added -swf-lib for importing SWF library
* added neko.db package

##### 2005-12-23: __alpha 5__

* added -main commandline parameter
* catches are now working with Neko
* restricted catch types for type-safety
* added constructor inheritance + check if superconstructor is called
* allowed Dynamic-only subtyping on type parameters
* added method closures to Neko generation
* added class Reflect
* added License : libraries are BSD
* added -xml documentation output
* allowed class instance :> anonymous subtyping

##### 2005-12-10: __alpha 4__

* forbid break and continue outside loops
* fixed SWF generation bugs
* added SWF "extends" support
* added method closures
* added some flash lowlevel operations (__xxx__)
* added Log, LogInfos and trace
* added Neko generation
* fixed problems with conditional compilation macros

##### 2005-11-30: __alpha 3__

* added Flash extern classes
* Boot initialization
* added "untyped"
* added conditional compilation
* added interfaces
* changed iterators from closures to objects
* added (XML)Node and XmlParser for Flash

##### 2005-11-25: __alpha 2__

* swf generation (missing iterators)
* some typing fixes

##### 2005-11-17: __alpha 1b__

* fix some bugs
* changed package tests.lang

##### 2005-11-14: __alpha 1__

* lexer
* parser
* typer
