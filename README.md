import React from "react";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Card, CardContent } from "@/components/ui/card";
import { School } from "lucide-react";

export default function HomePage() {
  return (
    <div className="min-h-screen bg-gray-50 p-6">
      <header className="mb-10 text-center">
        <h1 className="text-4xl font-bold mb-2">SchoolDekho.com</h1>
        <p className="text-lg text-gray-600">Find the best school for your child – smart, simple, and reliable.</p>
      </header>

      <section className="mb-10 flex flex-col items-center">
        <div className="flex w-full max-w-xl space-x-2">
          <Input placeholder="Search by school name, city, or board" />
          <Button>Search</Button>
        </div>
      </section>

      <section className="grid grid-cols-1 md:grid-cols-3 gap-6">
        <Card>
          <CardContent className="p-4">
            <School className="h-8 w-8 text-blue-500 mb-2" />
            <h3 className="text-xl font-semibold mb-1">Browse Schools</h3>
            <p className="text-gray-600 text-sm">Explore top schools by board, city, fee, and facilities.</p>
          </CardContent>
        </Card>

        <Card>
          <CardContent className="p-4">
            <School className="h-8 w-8 text-green-500 mb-2" />
            <h3 className="text-xl font-semibold mb-1">Admission Alerts</h3>
            <p className="text-gray-600 text-sm">Never miss deadlines – get updates on open admissions.</p>
          </CardContent>
        </Card>

        <Card>
          <CardContent className="p-4">
            <School className="h-8 w-8 text-purple-500 mb-2" />
            <h3 className="text-xl font-semibold mb-1">Parent Reviews</h3>
            <p className="text-gray-600 text-sm">Real reviews by parents to help you make informed choices.</p>
          </CardContent>
        </Card>
      </section>

      <footer className="mt-16 text-center text-gray-400 text-sm">
        &copy; {new Date().getFullYear()} SchoolDekho.com. All rights reserved.
      </footer>
    </div>
  );
}
