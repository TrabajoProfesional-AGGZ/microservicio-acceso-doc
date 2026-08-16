---
layout: default
title: Endpoints
nav_order: 2
---

# 🔌 Endpoints

En esta sección se listan los endpoints disponibles en el microservicio de accesos.

Esta página sirve como referencia estática para garantizar el acceso a los contratos de la API de forma rápida y clara.

## Listado de Endpoints

A continuación, haz clic en cada bloque para desplegar los detalles de la petición, parámetros y respuestas.

<details>
  <summary style="font-size: 1.1em; cursor: pointer; padding: 10px; background-color: #f8f9fa; border-radius: 4px; border-left: 4px solid #007bff; margin-bottom: 5px;">
    <strong style="color: #007bff;">GET</strong> <code>/api/v1/accesos/health</code> - Health Check
  </summary>
  <div style="padding: 15px; border: 1px solid #f8f9fa; border-top: none; margin-bottom: 20px;">
    
    <p><strong>ID de la Operación:</strong> <code>health_check_api_v1_accesos_health_get</code></p>
    
    <p>Endpoint para verificar que el microservicio está funcionando correctamente.</p>

    <h3>Respuestas</h3>

    <p><strong>Código:</strong> <code>200 OK</code></p>
    <ul>
      <li><strong>Descripción:</strong> Successful Response</li>
      <li><strong>Content-Type:</strong> <code>application/json</code></li>
    </ul>

    <strong>Ejemplo de respuesta:</strong>
    <div class="language-json highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="p">{}</span>
</code></pre></div></div>

  </div>
</details>

<details>
  <summary style="font-size: 1.1em; cursor: pointer; padding: 10px; background-color: #f8f9fa; border-radius: 4px; border-left: 4px solid #28a745; margin-bottom: 5px;">
    <strong style="color: #28a745;">POST</strong> <code>/api/v1/accesos/enrolar</code> - Enrolar Dispositivo
  </summary>
  <div style="padding: 15px; border: 1px solid #f8f9fa; border-top: none; margin-bottom: 20px;">
    
    <p><strong>ID de la Operación:</strong> <code>enrolar_dispositivo_api_v1_accesos_enrolar_post</code></p>
    
    <p>Endpoint para asociar o enrolar el dispositivo o token de un socio en el sistema de accesos.</p>

    <h3>Cuerpo de la Petición (Request Body)</h3>
    <p><strong>Content-Type:</strong> <code>application/json</code> (Requerido)</p>

    <div class="language-json highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="p">{</span><span class="w">
  </span><span class="nl">"socio_id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"string"</span><span class="w"> </span><span class="err">// Obligatorio</span><span class="w">
</span><span class="p">}</span>
</code></pre></div></div>

    <h3>Respuestas</h3>

    <p><strong>Código:</strong> <code>200 OK</code></p>
    <ul>
      <li><strong>Descripción:</strong> Successful Response</li>
    </ul>
    <div class="language-json highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="p">{}</span>
</code></pre></div></div>

    <p><strong>Código:</strong> <code>422 Unprocessable Entity</code></p>
    <ul>
      <li><strong>Descripción:</strong> Validation Error</li>
    </ul>
    <div class="language-json highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="p">{</span><span class="w">
  </span><span class="nl">"detail"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span><span class="w">
    </span><span class="p">{</span><span class="w">
      </span><span class="nl">"loc"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span><span class="s2">"string"</span><span class="p">,</span><span class="w"> </span><span class="mi">0</span><span class="p">],</span><span class="w">
      </span><span class="nl">"msg"</span><span class="p">:</span><span class="w"> </span><span class="s2">"string"</span><span class="p">,</span><span class="w">
      </span><span class="nl">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"string"</span><span class="w">
    </span><span class="p">}</span><span class="w">
  </span><span class="p">]</span><span class="w">
</span><span class="p">}</span>
</code></pre></div></div>

  </div>
</details>

<details>
  <summary style="font-size: 1.1em; cursor: pointer; padding: 10px; background-color: #f8f9fa; border-radius: 4px; border-left: 4px solid #28a745; margin-bottom: 5px;">
    <strong style="color: #28a745;">POST</strong> <code>/api/v1/accesos/validar</code> - Validar Acceso
  </summary>
  <div style="padding: 15px; border: 1px solid #f8f9fa; border-top: none; margin-bottom: 20px;">
    
    <p><strong>ID de la Operación:</strong> <code>validar_acceso_api_v1_accesos_validar_post</code></p>
    
    <p>Endpoint para validar un código QR u otra credencial y determinar si el socio tiene permitido el acceso, devolviendo su estado financiero e información de identidad.</p>

    <h3>Cuerpo de la Petición (Request Body)</h3>
    <p><strong>Content-Type:</strong> <code>application/json</code> (Requerido)</p>

    <div class="language-json highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="p">{</span><span class="w">
  </span><span class="nl">"qr_data"</span><span class="p">:</span><span class="w"> </span><span class="s2">"string"</span><span class="p">,</span><span class="w"> </span><span class="err">// Obligatorio</span><span class="w">
  </span><span class="nl">"id_evento"</span><span class="p">:</span><span class="w"> </span><span class="s2">"string"</span><span class="w"> </span><span class="err">// Opcional (null)</span><span class="w">
</span><span class="p">}</span>
</code></pre></div></div>

    <h3>Respuestas</h3>

    <p><strong>Código:</strong> <code>200 OK</code></p>
    <ul>
      <li><strong>Descripción:</strong> Successful Response</li>
    </ul>
    <div class="language-json highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="p">{</span><span class="w">
  </span><span class="nl">"status"</span><span class="p">:</span><span class="w"> </span><span class="s2">"string"</span><span class="p">,</span><span class="w">
  </span><span class="nl">"socio_id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"string"</span><span class="p">,</span><span class="w">
  </span><span class="nl">"nombre"</span><span class="p">:</span><span class="w"> </span><span class="s2">"string"</span><span class="p">,</span><span class="w">
  </span><span class="nl">"estado_financiero"</span><span class="p">:</span><span class="w"> </span><span class="s2">"string"</span><span class="p">,</span><span class="w">
  </span><span class="nl">"mensaje"</span><span class="p">:</span><span class="w"> </span><span class="s2">"string"</span><span class="w">
</span><span class="p">}</span>
</code></pre></div></div>

    <p><strong>Código:</strong> <code>422 Unprocessable Entity</code></p>
    <ul>
      <li><strong>Descripción:</strong> Validation Error</li>
    </ul>
    <div class="language-json highlighter-rouge"><div class="highlight"><pre class="highlight"><code><span class="p">{</span><span class="w">
  </span><span class="nl">"detail"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span><span class="w">
    </span><span class="p">{</span><span class="w">
      </span><span class="nl">"loc"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span><span class="s2">"string"</span><span class="p">,</span><span class="w"> </span><span class="mi">0</span><span class="p">],</span><span class="w">
      </span><span class="nl">"msg"</span><span class="p">:</span><span class="w"> </span><span class="s2">"string"</span><span class="p">,</span><span class="w">
      </span><span class="nl">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"string"</span><span class="w">
    </span><span class="p">}</span><span class="w">
  </span><span class="p">]</span><span class="w">
</span><span class="p">}</span>
</code></pre></div></div>

  </div>
</details>
