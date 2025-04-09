import React, { useState } from "react";
import { Card, CardContent } from "@mui/material";
import { Button } from "@mui/material";
import { Search } from "lucide-react";

const affiliateProducts = [
  {
    name: "Wireless Earbuds",
    description: "High-quality sound with noise cancellation.",
    image: "https://via.placeholder.com/150",
    link: "https://example.com/affiliate/earbuds"
  },
  {
    name: "Smartwatch",
    description: "Track your health and notifications on the go.",
    image: "https://via.placeholder.com/150",
    link: "https://example.com/affiliate/smartwatch"
  },
  {
    name: "Portable Charger",
    description: "Keep your devices powered up anytime, anywhere.",
    image: "https://via.placeholder.com/150",
    link: "https://example.com/affiliate/charger"
  }
];

export default function AffiliateSite() {
  const [searchTerm, setSearchTerm] = useState("");

  const filteredProducts = affiliateProducts.filter(product =>
    product.name.toLowerCase().includes(searchTerm.toLowerCase())
  );

  return (
    <div className="min-h-screen bg-gray-100 p-6">
      <header className="mb-6 text-center">
        <h1 className="text-3xl font-bold mb-2">Tech Deals Hub</h1>
        <p className="text-gray-600">Your go-to place for the best tech deals and affiliate offers.</p>
      </header>

      <div className="flex items-center max-w-md mx-auto mb-8">
        <input
          type="text"
          placeholder="Search deals..."
          value={searchTerm}
          onChange={e => setSearchTerm(e.target.value)}
          className="flex-1 p-2 border rounded"
        />
        <Button className="ml-2">
          <Search className="h-4 w-4" />
        </Button>
      </div>

      <div className="grid gap-6 grid-cols-1 md:grid-cols-3">
        {filteredProducts.map((product, idx) => (
          <Card key={idx} className="rounded-2xl shadow-md hover:shadow-lg transition">
            <CardContent className="p-4 text-center">
              <img src={product.image} alt={product.name} className="mx-auto mb-4 rounded-lg" />
              <h2 className="text-xl font-semibold mb-2">{product.name}</h2>
              <p className="text-gray-600 mb-4">{product.description}</p>
              <a href={product.link} target="_blank" rel="noopener noreferrer">
                <Button className="w-full" variant="contained" color="primary">
                  View Deal
                </Button>
              </a>
            </CardContent>
          </Card>
        ))}
      </div>
    </div>
  );
}
