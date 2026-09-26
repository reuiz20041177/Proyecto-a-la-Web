<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EduInclusiva - Plataforma Comunitaria</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-50 font-sans antialiased">

    <div class="flex h-screen overflow-hidden">
        
        <!-- Sidebar / Menú Lateral -->
        <aside class="w-64 bg-indigo-900 text-white flex flex-col justify-between hidden md:flex">
            <div>
                <div class="p-5 text-2xl font-bold tracking-wider border-b border-indigo-800 flex items-center space-x-2">
                    <span>📚 EduInclusiva</span>
                </div>
                <nav class="mt-5 space-y-1">
                    <button onclick="switchTab('inicio')" class="w-full text-left px-6 py-3 hover:bg-indigo-800 transition flex items-center space-x-3 tab-btn active-tab" id="btn-inicio">
                        <span>🏠</span> <span>Inicio</span>
                    </button>
                    <button onclick="switchTab('perfil')" class="w-full text-left px-6 py-3 hover:bg-indigo-800 transition flex items-center space-x-3 tab-btn" id="btn-perfil">
                        <span>👤</span> <span>Perfil y Registro</span>
                    </button>
                    <button onclick="switchTab('agendamiento')" class="w-full text-left px-6 py-3 hover:bg-indigo-800 transition flex items-center space-x-3 tab-btn" id="btn-agendamiento">
                        <span>📅</span> <span>Agendamiento</span>
                    </button>
                    <button onclick="switchTab('mensajeria')" class="w-full text-left px-6 py-3 hover:bg-indigo-800 transition flex items-center space-x-3 tab-btn" id="btn-mensajeria">
                        <span>💬</span> <span>Mensajería</span>
                    </button>
                    <button onclick="switchTab('admin')" class="w-full text-left px-6 py-3 hover:bg-indigo-800 transition flex items-center space-x-3 tab-btn" id="btn-admin">
                        <span>⚙️</span> <span>Panel Admin</span>
                    </button>
                </nav>
            </div>
            <div class="p-4 border-t border-indigo-800 text-xs text-indigo-300">
                ODS: Igualdad y Educación 🌍
            </div>
        </aside>

        <!-- Contenido Principal -->
        <div class="flex-1 flex flex-col overflow-y-auto">
            
            <!-- Header Superior -->
            <header class="bg-white shadow-sm h-16 flex items-center justify-between px-6">
                <h1 class="text-xl font-semibold text-gray-800" id="page-title">Bienvenido a EduInclusiva</h1>
                <div class="flex items-center space-x-4">
                    <span class="text-sm text-gray-600">Usuario Comunitario</span>
                    <div class="w-10 h-10 rounded-full bg-indigo-600 text-white flex items-center justify-center font-bold">U</div>
                </div>
            </header>

            <!-- Secciones Dinámicas -->
            <main class="p-6">
                
                <!-- SECCIÓN: INICIO -->
                <section id="content-inicio" class="section-content space-y-6">
                    <div class="bg-indigo-600 text-white p-8 rounded-xl shadow-md">
                        <h2 class="text-3xl font-bold mb-2">Educación sin barreras para todos</h2>
                        <p class="text-indigo-100 max-w-xl">Conectamos estudiantes, tutores voluntarios y recursos académicos accesibles para fomentar la igualdad de oportunidades en nuestra comunidad.</p>
                    </div>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                        <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-100">
                            <h3 class="font-bold text-lg text-gray-800 mb-1">Clases Accesibles</h3>
                            <p class="text-gray-600 text-sm">Reserva tutorías adaptadas a tus necesidades de aprendizaje.</p>
                        </div>
                        <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-100">
                            <h3 class="font-bold text-lg text-gray-800 mb-1">Comunidad Activa</h3>
                            <p class="text-gray-600 text-sm">Comunícate directamente con mentores y compañeros.</p>
                        </div>
                        <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-100">
                            <h3 class="font-bold text-lg text-gray-800 mb-1">Gestión Centralizada</h3>
                            <p class="text-gray-600 text-sm">Monitorea tu progreso académico en un solo lugar.</p>
                        </div>
                    </div>
                </section>

                <!-- SECCIÓN: PERFIL Y REGISTRO -->
                <section id="content-perfil" class="section-content hidden space-y-6">
                    <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-100 max-w-2xl mx-auto">
                        <h2 class="text-2xl font-bold text-gray-800 mb-4">Registro y Perfil Académico</h2>
                        <form class="space-y-4">
                            <div>
                                <label class="block text-sm font-medium text-gray-700">Nombre Completo</label>
                                <input type="text" class="mt-1 block w-full rounded-md border-gray-300 shadow-sm border p-2 focus:ring-indigo-500 focus:border-indigo-500" placeholder="Ej. Ana María Gómez">
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700">Correo Electrónico</label>
                                <input type="email" class="mt-1 block w-full rounded-md border-gray-300 shadow-sm border p-2" placeholder="correo@ejemplo.com">
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700">Rol en la Plataforma</label>
                                <select class="mt-1 block w-full rounded-md border-gray-300 shadow-sm border p-2">
                                    <option>Estudiante</option>
                                    <option>Tutor / Docente Voluntario</option>
                                    <option>Administrador</option>
                                </select>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700">Necesidades de Accesibilidad / Preferencias</label>
                                <textarea class="mt-1 block w-full rounded-md border-gray-300 shadow-sm border p-2" rows="3" placeholder="Indica si requieres intérprete, subtítulos, material adaptado, etc."></textarea>
                            </div>
                            <button type="button" class="w-full bg-indigo-600 text-white py-2 px-4 rounded-md hover:bg-indigo-700 transition">Guardar Perfil</button>
                        </form>
                    </div>
                </section>

                <!-- SECCIÓN: AGENDAMIENTO -->
                <section id="content-agendamiento" class="section-content hidden space-y-6">
                    <div class="bg-white p-6 rounded-xl shadow-sm border border-gray-100">
                        <h2 class="text-2xl font-bold text-gray-800 mb-4">Agendamiento de Tutorías</h2>
                        <p class="text-gray-600 mb-4">Selecciona una fecha y un tutor disponible para tu sesión de apoyo.</p>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div class="border p-4 rounded-lg">
                                <h3 class="font-semibold text-indigo-700">Matemáticas Básicas Inclusivas</h3>
                                <p class="text-sm text-gray-600">Tutor: Carlos Mendoza</p>
                                <p class="text-sm text-gray-500 mt-2">🕒 Próximo horario: Viernes 4:00 PM</p>
                                <button class="mt-4 bg-indigo-100 text-indigo-700 px-4 py-1.5 rounded text-sm font-medium hover:bg-indigo-200 transition">Agendar Cita</button>
                            </div>
                            <div class="border p-4 rounded-lg">
                                <h3 class="font-semibold text-indigo-700">Lectura y Apoyo en Lenguaje</h3>
                                <p class="text-sm text-gray-600">Tutor: Sofía Restrepo</p>
                                <p class="text-sm text-gray-500 mt-2">🕒 Próximo horario: Sábado 10:00 AM</p>
                                <button class="mt-4 bg-indigo-100 text-indigo-700 px-4 py-1.5 rounded text-sm font-medium hover:bg-indigo-200 transition">Agendar Cita</button>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- SECCIÓN: MENSAJERÍA -->
                <section id="content-mensajeria" class="section-content hidden space-y-6">
                    <div class="bg-white rounded-xl shadow-sm border border-gray-100 flex h-[500px]">
                        <div class="w-1/3 border-r p-4 overflow-y-auto">
                            <h3 class="font-bold text-gray-800 mb-3">Chats</h3>
                            <div class="p-2 hover:bg-gray-100 rounded cursor-pointer">
                                <p class="font-semibold text-sm">Carlos Mendoza</p>
                                <p class="text-xs text-gray-500">Nos vemos el viernes...</p>
                            </div>
                        </div>
                        <div class="w-2/3 flex flex-col justify-between p-4">
                            <div class="border-b pb-3 font-semibold text-gray-700">Conversación con Carlos Mendoza</div>
                            <div class="flex-1 overflow-y-auto py-4 space-y-3">
                                <div class="bg-gray-100 p-3 rounded-lg max-w-xs text-sm">Hola, ¿tienes alguna duda sobre el temario?</div>
                                <div class="bg-indigo-600 text-white p-3 rounded-lg max-w-xs text-sm ml-auto">Hola Carlos, todo claro por ahora. ¡Gracias!</div>
                            </div>
                            <div class="flex space-x-2 pt-2 border-t">
                                <input type="text" placeholder="Escribe un mensaje..." class="flex-1 border rounded-md p-2 text-sm">
                                <button class="bg-indigo-600 text-white px-4 py-2 rounded-md text-sm">Enviar</button>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- SECCIÓN: PANEL ADMIN -->
                <section id="content-admin" class="section-content hidden space-y-6">
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-6">
                        <div class="bg-white p-5 rounded-xl shadow-sm border">
                            <p class="text-sm text-gray-500">Usuarios Registrados</p>
                            <h3 class="text-2xl font-bold text-gray-800">124</h3>
                        </div>
                        <div class="bg-white p-5 rounded-xl shadow-sm border">
                            <p class="text-sm text-gray-500">Tutorías Activas</p>
                            <h3 class="text-2xl font-bold text-gray-800">18</h3>
                        </div>
                        <div class="bg-white p-5 rounded-xl shadow-sm border">
                            <p class="text-sm text-gray-500">Solicitudes Pendientes</p>
                            <h3 class="text-2xl font-bold text-gray-800">5</h3>
                        </div>
                    </div>
                    <div class="bg-white p-6 rounded-xl shadow-sm border">
                        <h2 class="text-xl font-bold text-gray-800 mb-4">Gestión de Usuarios y Reportes</h2>
                        <table class="w-full text-left border-collapse text-sm">
                            <thead>
                                <tr class="border-b text-gray-600">
                                    <th class="py-2">Nombre</th>
                                    <th class="py-2">Rol</th>
                                    <th class="py-2">Estado</th>
                                    <th class="py-2">Acciones</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr class="border-b">
                                    <td class="py-3">Juan Pérez</td>
                                    <td>Estudiante</td>
                                    <td><span class="bg-green-100 text-green-700 px-2 py-1 rounded text-xs">Activo</span></td>
                                    <td><button class="text-indigo-600 hover:underline">Editar</button></td>
                                </tr>
                                <tr class="border-b">
                                    <td class="py-3">María Gómez</td>
                                    <td>Tutor</td>
                                    <td><span class="bg-green-100 text-green-700 px-2 py-1 rounded text-xs">Activo</span></td>
                                    <td><button class="text-indigo-600 hover:underline">Editar</button></td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </section>

            </main>
        </div>
    </div>

    <!-- Script para cambiar de pestañas (Tabs) -->
    <script>
        function switchTab(tabId) {
            // Ocultar todas las secciones
            document.querySelectorAll('.section-content').forEach(el => el.classList.add('hidden'));
            // Mostrar la sección seleccionada
            document.getElementById('content-' + tabId).classList.remove('hidden');
            
            // Actualizar título superior
            const titles = {
                'inicio': 'Bienvenido a EduInclusiva',
                'perfil': 'Registro y Perfil Académico',
                'agendamiento': 'Módulo de Agendamiento',
                'mensajeria': 'Centro de Mensajería',
                'admin': 'Panel de Administración'
            };
            document.getElementById('page-title').innerText = titles[tabId];
        }
    </script>
</body>
</html>
