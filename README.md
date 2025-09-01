# tarea-maqueta
Este es el contenedor principal (el "marco" de todo).
.container-general {
    width: 600px;               /* ancho fijo de 600px */
    height: 500px;              /* alto fijo de 500px */
    background-color: #ffe599;  /* color de fondo (amarillo claro) */
    margin-top: 40px;           /* separación superior (margen arriba) */
    border-radius: 20px;        /* esquinas redondeadas */
    display: flex;              /* lo convierte en un contenedor flex */
    gap: 15px;                  /* separación entre los elementos hijos */
    border: 3px solid #000000;  /* borde negro de 3px */
    box-sizing: border-box;     /* incluye padding y borde dentro de width/height */
    padding: 15px;              /* espacio interno (relleno) */
    justify-self: center;       /* centra el contenedor dentro de su grid padre (si existe) */
}

Es una columna dentro del contenedor principal..columna-izquierda {
    display: flex;              /* también usa flexbox */
    flex-direction: column;     /* los hijos se apilan en columna */
    gap: 15px;                  /* separación entre sus elementos */
    flex: 2;                    /* ocupa el doble de espacio que la columna-derecha (flex 1) */
}

Es una fila dentro de .columna-izquierda, que contiene B y C.
.fila-bc {
    display: flex;              /* distribuye B y C en fila */
    gap: 15px;                  /* espacio entre ellos */
    flex: 4;                    /* ocupa más espacio vertical dentro de la columna izquierda */
}

Ajustes de tamaños de B y C:
.fila-bc .container-hijo:nth-child(2) {
    flex: 1.6;  /* C ocupa un poco más de espacio que B */
}
.fila-bc .container-hijo:nth-child(1) {
    flex: 1.2;  /* B ocupa un poco menos */
}

Es la columna a la derecha.
.columna-derecha {
    display: flex;              /* usa flexbox */
    flex-direction: column;     /* se organiza en columna */
    gap: 15px;                  /* separación entre hijos */
    flex: 1;                    /* ocupa menos ancho que la columna izquierda */
}
.columna-derecha .container-hijo:nth-child(1) {
    flex: 1.4;  /* el primer hijo (arriba) más grande */
}
.columna-derecha .container-hijo:nth-child(2) {
    flex: 0.8;  /* el segundo hijo (abajo) más pequeño */
}

Son las “cajitas” internas (A, B, C, D, etc.).
.container-hijo {
    background-color: #f4cccc;  /* color rosado */
    border-radius: 15px;        /* bordes redondeados */
    display: flex;              /* para centrar el contenido */
    justify-content: center;    /* centra el texto horizontalmente */
    align-items: center;        /* centra el texto verticalmente */
    font-size: 36px;            /* tamaño del texto */
    font-weight: bold;          /* texto en negrita */
    flex: 1;                    /* por defecto ocupa el mismo tamaño que otros, salvo que se sobrescriba */
    border: 2px solid #000000;  /* borde negro */
}

