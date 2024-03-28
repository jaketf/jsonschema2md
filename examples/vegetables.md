# JSON Schema

*Vegetable preferences*

## Additional Properties

- **Additional Properties** *(object)*: Additional info about foods you may like.
  - **`^iLike(Meat|Drinks)$`** *(boolean)*: Do I like it?
## Properties

- **`fruits`** *(array)*
  - **Items** *(string)*
- **`vegetables`** *(array)*
  - **Items**: Refer to *#/definitions/veggie*.
## Definitions

- **`veggie`** *(object)*
  - **`veggieName`** *(string)*: The name of the vegetable.
  - **`veggieLike`** *(boolean)*: Do I like this vegetable?
## Dependencies

- **`fruits`**
  - **One of**
    - **Must be one of: `apple`, `banana`.**
      - **toppings**: `peanut butter`, `caramel`, `honey`
    - **`orange`**
      - **toppings**: `peanut butter`, `caramel`
## Examples

  ```json
  {
      "fruits": [
          "apple",
          "orange"
      ],
      "vegetables": [
          {
              "veggieName": "cabbage",
              "veggieLike": true
          }
      ]
  }
  ```
