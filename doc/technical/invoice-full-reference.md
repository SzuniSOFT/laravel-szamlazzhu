# Invoice full reference

## Fields

### Attributes

| Field name           | Default value |
|----------------------|---------------|
| comment              | `''`          |
| createdAt            | `null`        |
| currency             | `'EUR'`       |
| fulfillmentAt        | `null`        |
| invoiceLanguage      | `'en'`        |
| isElectronic         | `true`        |
| isFinalInvoice       | `false`       |
| isImprestInvoice     | `false`       |
| isPaid               | `false`       |
| isPrepaymentRequest  | `false`       |
| isReplacementInvoice | `false`       |
| paymentDeadline      | `null`        |

### Protected

| Field name                | Default value |
|---------------------------|---------------|
| cancellationInvoice       | `null`        |
| cancellationInvoiceNumber | `null`        |
| proFormaInvoice           | `null`        |
| proFormaInvoiceNumber     | `null`        |

## Methods

| Method name              | Return one of these                                           | Parameters                                                                                                                      |
|--------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| cancel()                 | `Invoice`                                                     | `$withoutPdf = false`<br> `$emailSubject = null`<br> `$emailMessage = null`<br> `InvoiceCancellationResponse &$response = null` |
| getCancellationInvoice() | `null`<br>`AbstractInvoice`<br>`Invoice`<br>`ProformaInvoice` |                                                                                                                                 |
| getProFormaInvoice()     | `null`<br>`ProformaInvoice`                                   |                                                                                                                                 |
| save()                   | `Invoice`                                                     | `$withoutPdf = false`<br> `$emailSubject = null`<br> `$emailMessage = null`<br> `InvoiceCreationResponse &$response = null`     |
| update()                 | `Invoice`                                                     |                                                                                                                                 |