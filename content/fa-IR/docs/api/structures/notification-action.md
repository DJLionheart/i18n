# شئ NotificationAction

* `نوع` رشته - نوعی عمل، که می تواند `دکمه` باشد.
* `text` String (optional) - برچب عمل.

## پلت فرم / پشتیبانی عمل

| نوع عمل | پشتیبانی پلت فرم | `متن` - مورد استفاده         | `متن` پیشفرض                                                                                | محدودیت ها                                                                                                                                                                                                                                                                                             |
| ------- | ---------------- | ---------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `دکمه`  | سیستم عامل مک    | برچسب مورد استفاده برای دکمه | "Show" (or a localized string by system default if first of such `button`, otherwise empty) | فقط اولی استفاده می‌شود. اگر چندتا داده شوند، آن هایی که بعد از اولی هستند به عنوان عمل های اضافی لیست خواهند شد. (وقتی که موس روی دکمه عمل فعال باشد نمایش داده می‌شوند). عمل های این چنینی با `hasReply` سازگار نیستند و در صورتی که شرط `hasReply` is `true` برقرار نباشد، از آنها چشم پوشی می‌شود. |

### پشتیبانی دکمه در مک‌اواس

به منظور استفاده از دکمه در مک‌اواس، برنامه شما باید شرایط زیر داشته باشد.

* برنامه حضور داشته باشد
* App has it's `NSUserNotificationAlertStyle` set to `alert` in the `Info.plist`.

اگر هر یک از این نیاز ها برآورده نشده باشد، دکمه ظاهر نخواهد شد.