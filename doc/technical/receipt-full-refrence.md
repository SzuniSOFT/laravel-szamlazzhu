# Receipt full reference

## Fields

### Attributes

| Field name | Default value |
|------------|---------------|
| currency   | `'EUR'`       |

### Protected

| Field name            | Default value |
|-----------------------|---------------|
| cancellationReceipt   | `null`        |
| originalReceipt       | `null`        |

## Methods

| Method name              | Return one of these | Parameters                                                                |
|--------------------------|---------------------|---------------------------------------------------------------------------|
| getOriginalReceipt()     | `Receipt|null`      |                                                                           |
| getCancellationReceipt() | `null`<br>`self`    |                                                                           |
| hasOriginalReceipt()     | `bool`              |                                                                           |
| validateForSave()        | `$this`             |                                                                           |
| update()                 | `Receipt`           | `$withoutPdf = false`                                                     |
| save()                   | `Receipt`           | `$withoutPdf = false`,<br>`ReceiptCreationResponse &$response = null`     |
| cancel()                 | `Receipt`           | `$withoutPdf = false`,<br>`ReceiptCancellationResponse &$response = null` |

