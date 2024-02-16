### Como crear formularios


<section>
      <h2>Formulario de contacto</h2>
      <form method="post" action="/">
        <fieldset>
          <legend>Información personal</legend>
          <div>
            <label>Nombre:
              <input type="text" name="name" placeholder="Miguel Ángel Durán" required>
            </label>
          </div>
          <label>Email:
            <input type="email" name="email" placeholder="midudev@gmail.com" required>
          </label>
        </fieldset>
        <fieldset>
          <legend>Información adicional</legend>
          <div>
            <label>Teléfono:
              <input type="tel" name="phone" placeholder="Miguel Ángel Durán" required pattern="[0-9]{9}">
            </label>
          </div>
        </fieldset>
        <fieldset>
          <legend>Otros</legend>
          <div>
            <label for="why">¿Por qué quieres contactar?</label>
            <select name="why" id="why">
              <option value="1">Trabajo</option>
              <option value="2">Duda</option>
              <option value="3">Más información</option>
            </select>
          </div>
          <div>
            <label for="terms">¿Aceptas los términos?</label>
            <input type="checkbox" id="terms" name="terms" required>
          </div>
          <div>
            <datalist id="languages">
              <option value="JavaScript"></option>
              <option value="Python"></option>
              <option value="Java"></option>
              <option value="C#"></option>
            </datalist>
            <label>
              ¿Con qué lenguaje quieres que te ayude?
              <input list="languages" name="languages">
            </label>
          </div>
        </fieldset>
        <button>Enviar contacto</button>
      </form>
    </section>

```html
<section>
      <h2>Formulario de contacto</h2>

      <form method="post" action="/">
        <fieldset>
          <legend>Información personal</legend>

          <div>
            <label>Nombre:
              <input type="text" name="name" placeholder="Miguel Ángel Durán" required>
            </label>
          </div>

          <label>Email:
            <input type="email" name="email" placeholder="midudev@gmail.com" required>
          </label>
        </fieldset>

        <fieldset>
          <legend>Información adicional</legend>
          <div>
            <label>Teléfono:
              <input type="tel" name="phone" placeholder="Miguel Ángel Durán" required pattern="[0-9]{9}">
            </label>
          </div>
        </fieldset>

        <fieldset>
          <legend>Otros</legend>

          <div>
            <label for="why">¿Por qué quieres contactar?</label>
            <select name="why" id="why">
              <option value="1">Trabajo</option>
              <option value="2">Duda</option>
              <option value="3">Más información</option>
            </select>
          </div>

          <div>
            <label for="terms">¿Aceptas los términos?</label>
            <input type="checkbox" id="terms" name="terms" required>
          </div>

          <div>
            <datalist id="languages">
              <option value="JavaScript"></option>
              <option value="Python"></option>
              <option value="Java"></option>
              <option value="C#"></option>
            </datalist>
            <label>
              ¿Con qué lenguaje quieres que te ayude?
              <input list="languages" name="languages">
            </label>
          </div>
        </fieldset>

        <button>Enviar contacto</button>
      </form>
    </section>
```
Existen 2 formas de hacer lo mismo
```html
    <label> Email:
        <input type="email" name="email"
        placeholder="fernando.parra@uc.cl" required>
    </label>

    <label for="name">Nombre:</label>
    <input 
        type="text" 
        id="name" 
        name="name" 
        placeholder="Fernando Parra" 
        required
    >
```
El `required` es para señalar que es un campo obligatorio.
`<form method="post" action="/">` "post" es para señalar que era un formulario, y en action se pone el enlace a donde se va a enviar el formulario.

Importante colocar el `type="email" o type="tel"` para que se se autorellene o se verifique 