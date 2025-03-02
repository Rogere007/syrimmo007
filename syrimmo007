import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";
import { useState } from "react";

const properties = [
  { id: 1, title: "Appartement Moderne", location: "Kinshasa", price: "500$/mois", image: "https://source.unsplash.com/400x300/?apartment" },
  { id: 2, title: "Villa Luxueuse", location: "Lubumbashi", price: "2000$/mois", image: "https://source.unsplash.com/400x300/?villa" },
  { id: 3, title: "Terrain à Vendre", location: "Goma", price: "50 000$", image: "https://source.unsplash.com/400x300/?land" }
];

const HomePage = () => {
  const [showContact, setShowContact] = useState(false);

  return (
    <div className="min-h-screen bg-gray-100">
      <header className="bg-blue-600 text-white py-6 text-center text-3xl font-bold">
        SYR CONGO IMMO - Agence Immobilière Gratuite
      </header>

      <section className="p-10 grid grid-cols-1 md:grid-cols-3 gap-6">
        {properties.map((property) => (
          <motion.div
            key={property.id}
            whileHover={{ scale: 1.05 }}
            className="shadow-lg rounded-2xl overflow-hidden"
          >
            <Card>
              <CardContent className="p-0">
                <img
                  src={property.image}
                  alt={property.title}
                  className="w-full h-60 object-cover"
                />
                <div className="p-4">
                  <h3 className="text-xl font-semibold">{property.title}</h3>
                  <p className="text-gray-600">{property.location}</p>
                  <p className="text-blue-600 font-bold">{property.price}</p>
                  <Button className="mt-4" onClick={() => setShowContact(true)}>Contact</Button>
                </div>
              </CardContent>
            </Card>
          </motion.div>
        ))}
      </section>

      {showContact && (
        <div className="bg-white p-6 rounded-xl shadow-lg fixed bottom-10 right-10 max-w-md">
          <h2 className="text-2xl font-semibold mb-4">Contactez-nous</h2>
          <p>Email : contact@syrcongoimmo.com</p>
          <p>Téléphone : +243 970 000 000</p>
          <Button className="mt-4" onClick={() => setShowContact(false)}>Fermer</Button>
        </div>
      )}

      <footer className="bg-blue-600 text-white text-center py-4">
        © 2025 SYR CONGO IMMO - Tous droits réservés.
      </footer>
    </div>
  );
};

export default HomePage;
