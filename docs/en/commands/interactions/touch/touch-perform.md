[//]: # (DO NOT EDIT THIS FILE! This is an auto-generated file. Editing for this document happens in /commands-yml/commands/interactions/touch/touch-perform.yml)
# Touch Perform

Perform a touch action sequence
[//]: # (DO NOT EDIT THIS FILE! This is an auto-generated file. Editing for this document happens in /commands-yml/commands/interactions/touch/touch-perform.yml)
## Example Usage

```java
// Java
TouchAction action = new TouchAction(driver);
action.press(10, 10);
action.moveTo(10, 100);
action.release();
action.perform();

```

```python
# Python
from appium.webdriver.common.touch_action import TouchAction
// ...
actions = TouchAction(driver)
actions.tap_and_hold(20, 20)
actions.move_to(10, 100)
actions.release()
actions.perform()

```

```javascript
// Javascript
// webdriver.io example
driver.touchPerform([
  { action: 'press', options: { x: 100, y: 250 }},
  { action: 'moveTo', options: { x: 300, y: 100 }},
  { action: 'release' }
]);

// wd example
let action = new wd.TouchAction();
action.press({x: 10, y: 10});
action.moveTo({x: 10, y: 100});
action.release();
await action.perform();

```

```ruby
# Ruby
# ruby_lib example
touch_action.down(element).move_to(10, 100).up(50, 50).perform

# ruby_lib_core example
@driver.touch_action.down(element).move_to(10, 100).up(50, 50).perform

```

```csharp
// C#
TouchAction action = new TouchAction(driver);
action.Press(10, 10);
action.MoveTo(10, 100);
action.Release();
action.Perform();

```

[//]: # (DO NOT EDIT THIS FILE! This is an auto-generated file. Editing for this document happens in /commands-yml/commands/interactions/touch/touch-perform.yml)
## Description

This functionality is only available from within a native context

'Touch Perform' works similarly to the other singular touch interactions, except that this allows you to chain together more than one touch action as one
command. This is useful because Appium commands are sent over the network and there's latency between commands. This latency can make certain touch
interactions impossible because some interactions need to be performed in one sequence. Vertical, for example, requires pressing down, moving to a different
y coordinate, and then releasing. For it to work, there can't be a delay between the interactions.


[//]: # (DO NOT EDIT THIS FILE! This is an auto-generated file. Editing for this document happens in /commands-yml/commands/interactions/touch/touch-perform.yml)
## Support

[//]: # (DO NOT EDIT THIS FILE! This is an auto-generated file. Editing for this document happens in /commands-yml/commands/interactions/touch/touch-perform.yml)
### Appium Server

|Platform|Driver|Platform Versions|Appium Version|Driver Version|
|--------|----------------|------|--------------|--------------|
| iOS | [XCUITest](/docs/en/drivers/ios-xcuitest.md) | 9.3+ | 1.6.0+ | All |
|  | [UIAutomation](/docs/en/drivers/ios-uiautomation.md) | 8.0 to 9.3 | All | All |
| Android | [Espresso](/docs/en/drivers/android-espresso.md) | ?+ | 1.9.0+ | All |
|  | [UiAutomator2](/docs/en/drivers/android-uiautomator2.md) | ?+ | 1.6.0+ | All |
|  | [UiAutomator](/docs/en/drivers/android-uiautomator.md) | 4.3+ | All | All |
| Mac | [Mac](/docs/en/drivers/mac.md) | ?+ | 1.6.4+ | All |
| Windows | [Windows](/docs/en/drivers/windows.md) | 10+ | 1.6.0+ | All |


[//]: # (DO NOT EDIT THIS FILE! This is an auto-generated file. Editing for this document happens in /commands-yml/commands/interactions/touch/touch-perform.yml)
### Appium Clients

|Language|Support|Documentation|
|--------|-------|-------------|
|[Java](https://github.com/appium/java-client/releases/latest)| All | [appium.github.io](https://appium.github.io/java-client/io/appium/java_client/TouchAction.html) |
|[Python](https://github.com/appium/python-client/releases/latest)| All | [appium.github.io](https://appium.github.io/python-client-sphinx/webdriver.common.html#module-webdriver.common.touch_action) |
|[Javascript (WebdriverIO)](http://webdriver.io/index.html)| All |  |
|[Javascript (WD)](https://github.com/admc/wd/releases/latest)| All | [github.com](https://github.com/admc/wd/blob/master/lib/commands.js#L1546) |
|[Ruby](https://github.com/appium/ruby_lib/releases/latest)| All | [www.rubydoc.info](https://www.rubydoc.info/github/appium/ruby_lib/Appium/TouchAction) |
|[C#](https://github.com/appium/appium-dotnet-driver/releases/latest)| All | [github.com](https://github.com/appium/appium-dotnet-driver/blob/master/src/Appium.Net/Appium/MultiAction/TouchAction.cs) |

[//]: # (DO NOT EDIT THIS FILE! This is an auto-generated file. Editing for this document happens in /commands-yml/commands/interactions/touch/touch-perform.yml)
## HTTP API Specifications

[//]: # (DO NOT EDIT THIS FILE! This is an auto-generated file. Editing for this document happens in /commands-yml/commands/interactions/touch/touch-perform.yml)
### Endpoint

`POST /session/:session_id/touch/perform`

[//]: # (DO NOT EDIT THIS FILE! This is an auto-generated file. Editing for this document happens in /commands-yml/commands/interactions/touch/touch-perform.yml)
### URL Parameters

|name|description|
|----|-----------|
|session_id|ID of the session to route the command to|

[//]: # (DO NOT EDIT THIS FILE! This is an auto-generated file. Editing for this document happens in /commands-yml/commands/interactions/touch/touch-perform.yml)
### JSON Parameters

|name|type|description|
|----|----|-----------|
| action | `string` | The type of action to perform (moveTo\|release\|press\|tap\|wait) |
| options | `object` | The parameters of the action |
| opts.element | `string` | The ID of the element |
| opts.x | `number` | The X coordinate of the operation (relative to top left corner) |
| opts.y | `number` | The Y coordinate of the operation (relative to top left corner) |
| opts.count | `number` | Tap count |

[//]: # (DO NOT EDIT THIS FILE! This is an auto-generated file. Editing for this document happens in /commands-yml/commands/interactions/touch/touch-perform.yml)
### Response

null

[//]: # (DO NOT EDIT THIS FILE! This is an auto-generated file. Editing for this document happens in /commands-yml/commands/interactions/touch/touch-perform.yml)
## See Also

* [JSONWP Specification](https://github.com/appium/appium-base-driver/blob/master/lib/protocol/routes.js#L346)
