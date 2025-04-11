
## 🧪 **Caso práctico: decisiones en acción (Simon + Fayol + Bash)**

### 🧭 Contexto:
- Vos sos el técnico de soporte.
- Tenés que implementar un sistema de backup diario de las carpetas de cada docente a un servidor central.
- No hay mucho tiempo ni presupuesto.
- Usás software libre.

---

## 💡 ¿Cómo se conectan las teorías?

### 🧠 **Herbert Simon (Teoría del Comportamiento)**
> “La toma de decisiones debe adaptarse a la realidad limitada.”

- No vas a buscar *la solución perfecta*, sino una que **funcione bien con los recursos que tenés**.
- Elegís automatizar con **scripts en Bash y cron**.
- Decidís hacer backups incrementales con `rsync` porque es **rápido y confiable**, aunque no sea lo más avanzado.

```bash
#!/bin/bash
rsync -avz /home/docentes/ guillenec@servidor:/backups/$(date +%F)/
```

---

### 📐 **Frederick Taylor (Administración Científica)**
> “Estandarizar y racionalizar el trabajo mejora la eficiencia.”

- Armás un **script estándar** que todos los servidores puedan usar.
- Lo documentás bien: qué hace, cuándo corre, cómo restaurar datos.
- Lo dejás automatizado con `cron`:

```bash
0 20 * * * /home/guillenec/scripts/backup.sh
```

---

### 🏭 **Henri Fayol (Teoría Clásica)**
> “Administrar es prever, organizar, coordinar y controlar.”

- Prever: analizás riesgos de pérdida de info.
- Organizar: distribuís carpetas, accesos, y permisos.
- Coordinar: hablás con el equipo para saber cuándo es mejor que corra.
- Control: hacés logs de los backups y te mandás alertas por mail si falla:

```bash
rsync -avz /home/docentes/ servidor:/backups | tee /var/log/backup.log
```

---

### 🤝 **Teoría Humanista (Mayo)**
> “Las personas trabajan mejor si sienten que su trabajo importa.”

- Le explicás a los profes lo que hiciste.
- Les mostrás cómo acceder a sus backups.
- Les das tranquilidad: “No van a perder sus cosas si se rompe la compu”.

---

## 🚀 Resultado
Creaste un proceso simple, eficiente, basado en buenas decisiones, que considera:
- lo técnico (bash, scripts, cron),
- lo humano (la confianza del equipo),
- y lo organizacional (automatización, documentación, monitoreo).

