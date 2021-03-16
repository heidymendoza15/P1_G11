# UNIVERSIDAD SAN CARLOS DE GUATEMALA
# FACULTAD DE INGENIERIA
# ANALISIS Y DISEÑO 1
# PRACTICA 2

<<<<<<< Updated upstream
###### HEIDY LISSETH MENDOZA CARDONA   201503811

# Manual Tecnico

Lenguaje utilizado:
- FRONT END: Angular-TypeScript
- BACK  END: Flask-Python

Herramienta para pruebas:
- Jasmine-Karma
=======
### Integrantes

- 201020397	Kevin Josue Hernandez Gomez
- 201020831	Marco Antonio Fidencio Chávez Fuentes
- 201503811	Heidy Lisseth Mendoza Cardona
- 201612331	Josè Orlando Wannan Escobar
- 201700965	José Carlos I Alonzo Colocho
- 201730555	Francisco Javier Bran Fuentes

# Manual Tecnico

### Lenguaje utilizado:
- FRONT END: Angular-TypeScript
- BACK  END: Flask-Python
- BD: MySQL
	
### Herramienta para pruebas:
  - Jasmine-Karma

## INDICE
1. [Login](#login)
2. [Registro](#registro)
3. [Blog - Publicaciones](#publicaciones-y-blog)
4. [Pruebas Unitarias](#pruebas-unitarias)
5. [Code Coverage](#code-coverage)


>>>>>>> Stashed changes

## Login 

Para el login se utilizó una prueba unitaria de HttpClient para verificar que la tarea se maneje correctamente utilizando Angular TestBed que configura un entorno bajo prueba que utilizar el modulo HttpClientTestModule en lugar del HttpClient module normal. Al finalizar se inyecta una referencia de HttpTestingController que nos permite manejar el comportamiento en el HttpClient que se ha simulado.

<<<<<<< Updated upstream

=======
```
  it('Login()', () => {

    //Arrange
    //Set Up Data
    const login:Logins = { username: 'Jose', password: '201612331' }
    const result = { 'status': 1, 'id': 1, 'user': 'Jose' }

    //Act
    service.Login(login).subscribe(
      (user)=>
      {
        //Assert-1
        expect(user).toEqual(result);
      }
    );

    //Assert -2
    const req = httpMock.expectOne(api.API_URI+ api.LOGIN);
    expect(req.request.method).toBe('POST');
    req.flush(result);
    //Assert -3
    httpMock.verify();

  });
```

## Registro

Para el Registro se utilizó una prueba unitaria de HttpClient para verificar que la tarea se maneje correctamente utilizando Angular TestBed que configura un entorno bajo prueba que utilizar el modulo HttpClientTestModule en lugar del HttpClient module normal. Al finalizar se inyecta una referencia de HttpTestingController que nos permite manejar el comportamiento en el HttpClient que se ha simulado.

```
    it('Register()', () => {

    //Arrange
    //Set Up Data
    const login: Usuario1 = { username: 'Jose1',fullname: 'Jose Wannan', photo: '', password: '201612331' }
    const result = { 'status': 1}

    //Act
    service.Create(login).subscribe(
      (user)=>
      {
        //Assert-1
        expect(user).toEqual(result);
      }
    );

    //Assert -2
    const req = httpMock.expectOne(api.API_URI + api.REGISTRO);
    expect(req.request.method).toBe('POST');
    req.flush(result);
    //Assert -3
    httpMock.verify();

  });
```

## Publicaciones y Blog

Para el servicio de post se configuraron 2 tipos de test, para la creacion de una publicacion, y otro para obtener las publicaciones actualizadas.

Se genero una prueba unitaria de HttpClient para verificar que la tarea se maneje correctamente utilizando Angular TestBed que configura un entorno bajo prueba que utilizar el modulo HttpClientTestModule en lugar del HttpClient module normal. Al finalizar se inyecta una referencia de HttpTestingController que nos permite manejar el comportamiento en el HttpClient que se ha simulado.

```
  it('create() should call http Post method for the given route', () => {
    // ARRANGE
    // SET UP DATA
    const data: Publicacion = {
      Foto: 'miFoto.jpg',
      Contenido: 'Lorem ipsum',
      ID_Usuario: 1,
    };
    const result = { status: 1 };
    // ACT
    service.create(data).subscribe((post) => {
      expect(post).toEqual(result);
    });
    //Assert -2
    const req = httpMock.expectOne(
      (req) =>
        req.method == 'POST' && req.url === `${api.API_URI}${api.POSTEAR}`
    );
    expect(req.request.method).toBe('POST');
    req.flush(result);
    //Assert -3
    httpMock.verify();
  });
```

```
  it('getAll() should call http Get method for the given route', () => {
    // ARRANGE
    // SET TUP DATA
    const result = {
      status: 1,
      post: [
        {
          Contenido: 'Lorem ipsum',
          Foto: 'miFoto.jpg',
          ID_Usuario: 1,
          Fecha: 'Mon, 15/03/21 04:51:00 GTM',
        },
      ],
    };

    // ACT
    service.getAll().subscribe((post) => {
      expect(post).toEqual(result);
    });
    //Assert -2
    const req = httpMock.expectOne(
      (req) => req.method == 'GET' && req.url === `${api.API_URI}${api.POSTS}`
    );
    expect(req.request.method).toBe('GET');
    req.flush(result);
    //Assert -3
    httpMock.verify();
  });
```

Ademas, se manejo un test unitario para probar la ejecucion de los ErrorHandlers.

```
  it('throws 404 error', () => {
    service.handleError({
      headers: undefined,
      message: "",
      name: "HttpErrorResponse",
      ok: false,
      status: 0,
      statusText: "",
      type: undefined,
      url: undefined,
      error:'ErrorEvent'}).subscribe(
      data => fail('Should have failed with 404 error'),
      (error: HttpErrorResponse) => {
        expect(error.status).toEqual(undefined);
      }
    );

    const req = httpMock.expectNone(api.API_URI + '/Nadita');

  });
```


## Pruebas Unitarias

### Casos de prueba

![This is a alt text.](/images/im1.png "This is a sample image.")

![This is a alt text.](/images/im2.png "This is a sample image.")

![This is a alt text.](/images/im3.png "This is a sample image.")

![This is a alt text.](/images/im4.png "This is a sample image.")


- auth-service.spec.ts
- post-service.spec.ts

Se requeria de una configuración especifica desde los test para poder realizar los test satisfactoriamente.

```
  beforeEach(() => {
    TestBed.configureTestingModule({
      imports: [HttpClientTestingModule],
      providers: [PostService],
    });
    service = TestBed.inject(PostService);
    httpMock = TestBed.get(HttpTestingController);
    httpClient = TestBed.inject(HttpClient);
  });
```

## Code Coverage

Para definir el umbral de cobertura de codigo es necesario posicionarse en el documento **karma.conf.js**, y agregar la siguiente configuracion:

```
coverageIstanbulReporter: {
      reports: [ 'html', 'lcovonly' ],
      fixWebpackSourcePaths: true,
      thresholds: {
        statements: 85,
        lines: 85,
        branches: 85,
        functions: 85
      }
    }
```
>>>>>>> Stashed changes
