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
| isPrepaymentRequest  | `true`        |
| isReplacementInvoice | `false`       |
| paymentDeadline      | `null`        |


### Protected

| Field name   | Default value |
|--------------|---------------|
| orderInvoice | `null`        |


## Methods

| Method name       | Return one of these                       | Parameters                                                                                                                  |
|-------------------|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| orderInvoice()    | `AbstractInvoice|Invoice|ProformaInvoice` |                                                                                                                             |
| update()          | `ProformaInvoice`                         |                                                                                                                             |
| validateForSave() | `$this`                                   |                                                                                                                             |
| save()            | `ProformaInvoice`                         | `$withoutPdf = false`<br> `$emailSubject = null`<br> `$emailMessage = null`<br> `InvoiceCreationResponse &$response = null` |
| delete()          | `ProformaInvoice`                         | `ProformaInvoiceDeletionResponse &$response = null`                                                                         |
