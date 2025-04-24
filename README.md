// Basic structure for schooldekho.com
// React + Tailwind + Vite setup assumed

import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const schools = [
  {
    name: "Delhi Public School",
    location: "Delhi",
    board: "CBSE",
    rating: 4.5,
  },
  {
    name: "National Academy",
    location: "Mumbai",
    board: "ICSE",
    rating: 4.2,
  },
  {
    name: "Green Valley High",
    location: "Bangalore",
    board: "CBSE",
    rating: 4.7,
  },
];

export default function SchoolDekho() {
  return (
    <div className="min-h-screen bg-gray-50 p-6">
      <h1 className="text-4xl font-bold text-center mb-8">🏫 SchoolDekho.com</h1>
      <p className="text-center text-lg mb-6 text-gray-600">
        Discover the best schools near you. Filter by location, board, and rating.
      </p>
      <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-6 max-w-6xl mx-auto">
        {schools.map((school, index) => (
          <Card key={index} className="rounded-2xl shadow-lg">
            <CardContent className="p-4">
              <h2 className="text-xl font-semibold mb-2">{school.name}</h2>
              <p className="text-sm text-gray-700">📍 {school.location}</p>
              <p className="text-sm text-gray-700">🎓 Board: {school.board}</p>
              <p className="text-sm text-yellow-600">⭐ Rating: {school.rating}</p>
              <Button className="mt-4 w-full">View Details</Button>
            </CardContent>
          </Card>
        ))}
      </div>
    </div>
  );
}

