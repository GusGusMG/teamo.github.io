# Volver a crear y guardar los gráficos para asegurar que estén correctamente generados

# Gráfico de barras para preferencias de sabor
plt.figure(figsize=(8, 5))
plt.bar(sabores, aceptacion, color=["orange", "green", "red"])
plt.title("Preferencias de Sabor", fontsize=14)
plt.xlabel("Sabor", fontsize=12)
plt.ylabel("Aceptación (%)", fontsize=12)
plt.ylim(0, 100)
plt.grid(axis='y', linestyle="--", alpha=0.7)
plt.tight_layout()
preferencias_sabor_path = "/mnt/data/preferencias_sabor_v2.png"
plt.savefig(preferencias_sabor_path)
plt.close()

# Gráfico circular para percepción del diseño ecoamigable
plt.figure(figsize=(6, 6))
plt.pie(porcentaje_percepcion, labels=percepcion, autopct='%1.1f%%', startangle=90, colors=["blue", "gray"])
plt.title("Percepción del Diseño Ecoamigable", fontsize=14)
plt.tight_layout()
percepcion_sostenibilidad_path = "/mnt/data/percepcion_sostenibilidad_v2.png"
plt.savefig(percepcion_sostenibilidad_path)
plt.close()

preferencias_sabor_path, percepcion_sostenibilidad_path
